```ocaml
let shape_to_string: shape -> string =
  fun s -> Printf.sprintf "Shape(%F)" s#area;;
val shape_to_string : shape -> string = <fun>

let square_to_string: square -> string =
  (shape_to_string :> square -> string);;
val square_to_string : square -> string = <fun>
```