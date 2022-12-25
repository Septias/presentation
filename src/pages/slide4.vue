<template lang="pug">
slide
  div.flex.flex-col
    h1 Objekte in OCaml
    .flex
      div(class="w-1/2")
        example
          objectexample
      ul(class="w-1/2")
        //li Objekte und Klassen sind eine Möglichkeit von OCaml OOP anzuwenden
        li Objekte haben nicht wie andere Sprachen Klassentypen, sondern werden durch ihren
          span  Objekttyp
          |  beschrieben
        li
          | Der
          span  Objekttype
          |  wird durch die bereitgestellten Methoden festgelegt
        li
          span Methoden
          |  werden mit dem #-Operator aufgerufen
</template>
