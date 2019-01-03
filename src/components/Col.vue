<template>
    <div class="col" v-bind:style="{ flexGrow: size, flexBasis: minSize + 'px'}" @click="alertMe">
      <slot></slot>
    </div>
</template>

<script>
export default {
  name: 'Col',
  props: {
    size: {
      default: null,
      type: Number
    },
    minSize: {
      default: null,
      type: Number
    }
  },
  inject: ['alertMe'],
  methods: {

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
