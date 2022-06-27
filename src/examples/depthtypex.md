```ocaml
type circle = < area : float; radius : int >;;
type circle = < area : float; radius : int >

let circle r = object
  method area = 3.14 *. (Float.of_int r) **. 2.0
  method radius = r
end;;
val circle : int -> < area : float; radius : int > = <fun>

let coin = object
  method shape = circle 5
  method color = "silver"
end;;
val coin : < color : string; shape : < area : float; radius : int > > = <obj>

let map = object
  method shape = square 10
end;;
val map : < shape : < area : float; width : int > > = <obj>

type item = < shape : shape >;;
type item = < shape : shape >
let items = [ (coin :> item) ; (map :> item) ];;
val items : item list = [<obj>; <obj>]
```