<template>
  <div id="app">
    <Container direction="top">
      <Column minSize="100">aaa </Column>
      <Column >aaa </Column>
      <Column minSize="300">aaa </Column>
    </Container>
  </div>
</template>

<script>
import Container from './components/Container'
import Column from './components/Col'

export default {
  name: 'app',
  components: {
    Container,
    Column
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
