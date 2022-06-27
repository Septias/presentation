

```java
// Beispiel aus der Programmiersprache Java

// Eine Methode um den Typ von einem Objekt heraus zu bekommen
String GetShapeName(Shape s) {
  if (s instanceof Square) {
    return "Square";
  } else if (s instanceof Circle) {
    return "Circle";
  } else {
    return "Other";
  }
}
// Ein Test ob eine geometrische form eine Hantel ist
boolean IsBarbell(Shape[] s) {
  return s.length == 3 && (s[0] instanceof Circle) &&
    (s[1] instanceof Line) && (s[2] instanceof Circle) &&
        ((Circle) s[0]).radius() == ((Circle) s[2]).radius();
}
```

```ocaml
(** Der selbe Test in Ocaml mit Patternmatching umgesetzt *)
type shape = Circle of { radius : int } | Line of { length: int };;
type shape = Circle of { radius : int; } | Line of { length : int; }
let is_barbell = function
| [Circle {radius=r1}; Line _; Circle {radius=r2}] when r1 = r2 -> true
| _ -> false;;
val is_barbell : shape list -> bool = <fun>
```