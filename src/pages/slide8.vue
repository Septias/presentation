<template lang="pug">
slide
  div.flex.flex-col
    h1 Subtyping > Variance
    h2 Variance
    slide2sides
      template(v-slot:left)
        example
          variance
      template(v-slot:right)
        ul
          li Typen die aus Objekttypen konstruiert wurden, können auch genötigt werden
          li Ein
            |
            |
            code 'a list
            |  ist
            |
            span covariant
            |  (in 'a')
          li Ein
            |
            |
            code 'a array
            |  ist
            |
            span invariant.
    slide2sides
      template(v-slot:left)
        example
          variance2

    h2 Variance Annotations
    example
      varianceannotations
</template>
