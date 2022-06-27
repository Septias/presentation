<template lang="pug">
slide
  div.flex.flex-col
    h1 Narrowing (Downcasting)
    ul
      li Narrowing ist in OCaml grundsätzlich nicht erlaubt da
      li.ml-6 es schwer zu implementieren ist und
      li.ml-6 es zu unsauberem Code führt (es bricht Abstraktion)
      li
        | Es gibt einen verpönten Trick mit einer
        |
        code `variant`
        |  methode

    slide2sides
      template(v-slot:left)
        example.p-2
          badexample1
      template(v-slot:right)
        example.p-2
          badexample2
</template>
