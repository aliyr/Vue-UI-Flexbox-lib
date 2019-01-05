<template>
    <div
      class="col"
      v-bind:style="{ flexGrow: size, flexBasis: minSize}">
      <slot></slot>
    </div>
</template>

<script>
export default {
  name: 'Col',
  props: {
    size: {
      default: null,
      type: String
    },
    minSize: {
      default: null,
      type: String
    }
  }
}
</script>

<style scoped>
  .col{
    padding: 0 15px;
    border: 1px solid red;
    box-sizing: border-box;
  }
</style>
