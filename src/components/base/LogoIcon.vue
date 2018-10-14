<template>
  <svg width="32" height="32" xmlns="http://www.w3.org/2000/svg" xmlns:svg="http://www.w3.org/2000/svg">
   <g>
    <path d="m0,16l16,-16l0,16l-16,0z" :fill="this.topColor" id="svg_1"/>
    <path d="m31.86111,15.93056l-16,16l0,-16l16,0z" :fill="this.bottomColor" id="svg_2"/>
   </g>
  </svg>
</template>

<script>
export default {
  name: 'LogoIcon',
  props: ['topColor', 'bottomColor']
}
</script>

<style lang="scss">
svg {
  display: block;
}
</style>
