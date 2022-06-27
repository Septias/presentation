```ocaml
let squares: square list = [ square 10; square 20 ];;
val squares : square list = [<obj>; <obj>]

(** Diese Nötigung ist nur möglich, da der Listen immutable sind **)
let shapes: shape list = (squares :> shape list);;
val shapes : shape list = [<obj>; <obj>]
```