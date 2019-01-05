<template>
    <div
      class="container"
      :style="{flexDirection: fDirection}"
    >
      <slot></slot>
    </div>
</template>

<script>
export default {
  name: 'Container',
  props: {
    direction: {
      default: 'row',
      type: String
    }
  },
  computed: {
    fDirection () {
      switch (this.direction) {
        case 'left': {
          return 'row'
        }
        case 'right': {
          return 'row-reverse'
        }
        case 'top': {
          return 'column'
        }
        case 'bottom': {
          return 'column-reverse'
        }
      }
    }
  }
}
</script>

<style scoped>
  .container{
    width: 100%;
    height: auto;
    display: flex;
    box-sizing: border-box;
  }
</style>
