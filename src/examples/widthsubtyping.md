```ocaml
type shape = < area : float >;;
type square = < area : float; width : int >;;

let square w = object
  method area = Float.of_int (w * w)
  method width = w
end;;

(** Da beide Typen eine Methode `area` mit der selben Signatur
haben ist die Folgende Nötigung möglich: **)
(square 10 :> shape);;
```
