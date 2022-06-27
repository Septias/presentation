<template lang="pug">
slide
  div.flex.flex-col
    h1 Row Polymorphismus vs. Subtyping

    //slide2sides
      template(v-slot:left)
        h2 Row Poly

      template(v-slot:right)
        h2 Subtyping
    slide2sides
      template(v-slot:left)
        example
          proargpoly

      template(v-slot:right)
        ul
          li In den meisten Fällen wird Row Polymorphismus verwendet, da keine explizite Nötigung notwendig ist
          li Der implizierte Typ wird aus dem Objekttyp generiert, sodass alle zusätzlichen Methoden erhalten bleiben
    p Wenn man das selbe mit einem geschlossenen Objekttyp und Subtyping versucht, dann werden die übrigen Methoden nicht erhalten
    example
      subtypingbad

    p Mit Row Polymorphismus kann man keine Objekte mit verschiedenen Typen in eine Liste stecken
    example
      listexample
    p Dasselbe gilt auch für Referenzen
    example
      refexample
    p In diesen Fällen muss man Subtyping verwenden
    example
      subtypinggood
</template>
