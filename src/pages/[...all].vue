<script lang="ts" setup>
import Slide1 from './slide1.vue'
import Slide3 from './slide3.vue'
import Slide4 from './slide4.vue'
import Slide5 from './slide5.vue'
import Slide6 from './slide6.vue'
import Slide7 from './slide7.vue'
import Slide8 from './slide8.vue'
import Slide2 from './slide2.vue'
import Slide10 from './slide10.vue'
import Slide11 from './slide11.vue'
import Slide12 from './slide12.vue'
import Slide13 from './slide13.vue'
const router = useRouter()
// router.push('/slide1')
</script>

<template lang="pug">
div.width
    Slide1
    hr
    Slide2
    hr
    Slide3
    hr
    Slide4
    hr
    Slide5
    hr
    Slide6
    hr
    Slide7
    hr
    Slide8
    hr
    Slide10
    hr
    Slide11
    hr
    Slide12
    hr
    Slide13
    hr
</template>

<style lang="sass">
.width
  max-width: 1000px
</style>
