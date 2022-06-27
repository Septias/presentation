<template lang="pug">
slide
  h1 Wann verwendet man Objekte?
  p.text-xl Von den meisten erfahrenen Programmierern werden Objekte und Klassen wenig verwendet, da es mit Modulen, Funktoren und Datentypen
    | schon möglich ist ganz verschiedene Programmstrukturen zu erstellen. In Problemstellungen wo offene Rekursion wichtig ist, finden Klassen
    | und Objekte trotzdem Anwendung.
  .grid.grid-cols-2.gap-4
    div
      h2 First Class Modules
      ul
        li First Class Module sind aussagekräftiger als Objekte
        li First Class Module haben die Möglichkeit Typen zu definieren und mitzuliefern
        li Dafür erlauben Objekte Polymorphismus und Dynamic Dispatch
    div
      h2 Objects im Vergleich zu Records
      ul
        li Keine Typdefinitionen in Objekten
        li Objekte erlauben durch Polymorphismus höhere Flexibilität
        li Objekte haben eine relativ verbose Syntax
        li Objekte haben Runtimekosten
        p => Meisten werden Objekte nicht anstatt Records verwendet
</template>

<!--
**first class modules** sind aussagekräftiger und man hat noch die Möglichkeit typen zu definieren und mitzuliefern was mit Objekten nicht funktioniert.

Dafür erlauben Objekte Polymorphismus und dynamic dispatch

**objects vs. records**:
> Objects have some advantages over records: they don’t require type definitions,
and their support for row polymorphism makes them more flexible. However, the heavy syntax and additional runtime
cost means that objects are rarely used in place of records.

**objects vs. rest**:
> Modules, functors, and data types also offer a wide range of ways to express program structure.
In fact, many seasoned OCaml programmers rarely use classes and objects, if at all.

**Vorteile von Objekten**:
 -->
