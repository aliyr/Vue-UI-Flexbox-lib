<template>
    <div
      class="container"
      :style="{flexDirection: fDirection, alignItems: verticalAlign, justifyContent: horizontalAlign, flexWrap: wrap, width: width, height: height}"
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
    },
    horizontalAlign: {
      default: 'start',
      type: String
    },
    width: {
      default: '100%',
      type: String
    },
    height: {
      default: 'auto',
      type: String
    },
    verticalAlign: {
      default: 'start',
      type: String
    },
    isFlexible: {
      default: 'false',
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
    },
    wrap () {
      if (this.isFlexible === 'true') {
        return 'no-wrap'
      } else {
        return 'wrap'
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
