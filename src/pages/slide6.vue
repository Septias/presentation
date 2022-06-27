<template lang="pug">
slide
  div.flex.flex-col
    h1 Row Polymorphism

    slide2sides
      template(v-slot:left)
        example
          objpolyexample

      template(v-slot:right)
        ul
          li Funktionen können ohne explizite Typannotation definiert werden, da der Typ inferiert wird
          li
            code ..
            |  ist eine
            span  Row Variable
    slide2sides
      template(v-slot:left)
        example
          closedtypeex

      template(v-slot:right)
        ul
          li Objekttypen können explizit geschlossen werden
</template>
