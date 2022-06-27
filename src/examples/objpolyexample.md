```ocaml
let area sq = sq#width * sq#width;;
val area : < width : int; .. > -> int = <fun>

let minimize sq : unit = sq#resize 1;;
val minimize : < resize : int -> unit; .. > -> unit = <fun>

let limit sq = if (area sq) > 100 then minimize sq;;
val limit : < resize : int -> unit; width : int; .. > -> unit = <fun>
```