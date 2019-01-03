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
      default: 1,
      type: Number
    },
    minSize: {
      default: 0,
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
  }
</style>
