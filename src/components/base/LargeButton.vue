<template>
  <div class="button-container">
    <button class="button-large" :style="`background-color: ${backgroundColor}; border: 2px solid ${borderColor}`">
      <slot></slot>
    </button>
  </div>
</template>

<script>
export default {
  name: 'large-button',
  props: ['backgroundColor', 'borderColor']
}
</script>

<style lang="scss">

div.button-container {
  display: inline-block;
}

.button-large {
  width: 100px;
  height: 100px;
  border-radius: 100px;
  display: flex;
  justify-content: center;
  align-items: center;
  border: none;
  color: white;
  cursor: pointer;
}

</style>
