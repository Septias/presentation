<template lang="pug">
slide
  div.flex.flex-col
    h1 Subtyping
    blockquote.text-2xl
      | Subtyping is a central concept in object-oriented programming. It governs when an object with one type A can be used in an expression that expects an object of another type B

    h2 Width Subtyping
    slide2sides
      template(v-slot:left)
        example
          widthsubtyping

      template(v-slot:right)
        ul
          li
            | Der neue Operator
            |
            code ':>'
            |  erlaubt es nun ein Objekt A zu einem Objekt B zu machen.
          li Hier squar -> shape

    h2 Depth Subtyping
    slide2sides
      template(v-slot:left)
        example
          depthtypex

      template(v-slot:right)
        ul
          li Mit Depth Subtyping können wir ein Objekt A zu einem Objekt B machen, wenn die Methoden sicher verwandelt werden können.

    h2 Polymorphic Variant Subtyping
    slide2sides
      template(v-slot:left)
        variantsubtyping

      template(v-slot:right)
        ul
          li Man kann mit Subtyping auch polymorfische Varianten zu größeren polymorfischen Varianten vergrößern
          li Das geht wenn die Tags von A eine Untergruppe der Tags von B sind.
</template>
