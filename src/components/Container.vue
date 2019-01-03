<template>
    <div
      class="container"
      v-bind="$attrs"
    >
      <slot></slot>
    </div>
</template>

<script>
export default {
  name: 'Container',
  inheritAttrs: false,
  methods: {
    alertMe () {
      return { name: 'gholi' }
    }
  },
  provide: function () {
    return {
      alertMe: this.alertMe
    }
  }
}
</script>

<style scoped>
  .container{
    width: 200px;
    height: auto;
    display: flex;
  }
</style>
