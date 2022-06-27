```ocaml
(** Als erstes wird ein Type `Either` errstellt **)
module Either = struct
  type ('a, 'b) t =
    | Left of 'a
    | Right of 'b
  let left x = Left x
  let right x = Right x
end;;
module Either :
  sig
    type ('a, 'b) t = Left of 'a | Right of 'b
    val left : 'a -> ('a, 'b) t
    val right : 'a -> ('b, 'a) t
  end

(** Wenn man jetzt eine Nötigung versucht, funktionert das, da Either
covariant über 'a und 'b ist**)
let left_square = Either.left (square 40);;
val left_square : (< area : float; width : int >, 'a) Either.t =
  Either.Left <obj>
(left_square :> (shape,_) Either.t);;
- : (shape, 'a) Either.t = Either.Left <obj>


(** Nun erstellen wir uns einen Typ, der den Typ `t` hinter einer Signatur versteckt**)
module Abs_either : sig
  type ('a, 'b) t
  val left: 'a -> ('a, 'b) t
  val right: 'b -> ('a, 'b) t
end = Either;;


(** Aufgrund dessen muss Ocaml annehemen, dass die Parameter 'a und 'b invariant sind
und somit Assertions verbieten **)
(Abs_either.left (square 40) :> (shape, _) Abs_either.t);;
Line 1, characters 2-29:
Error: This expression cannot be coerced to type (shape, 'b) Abs_either.t;
       it has type (< area : float; width : int >, 'a) Abs_either.t
       but is here used with type (shape, 'b) Abs_either.t
       Type < area : float; width : int > is not compatible with type
         shape = < area : float >
       The second object type has no method width

(** Durch Variance Annotations können wir jetzt die Covarianz angeben, was wiederum die
Nötigung erlaubt **)
module Var_either : sig
  type (+'a, +'b) t
  val left: 'a -> ('a, 'b) t
  val right: 'b -> ('a, 'b) t
end = Either;;
module Var_either :
  sig
    type (+'a, +'b) t
    val left : 'a -> ('a, 'b) t
    val right : 'b -> ('a, 'b) t
  end

(Var_either.left (square 40) :> (shape, _) Var_either.t);;
- : (shape, 'a) Var_either.t = <abstr>
```