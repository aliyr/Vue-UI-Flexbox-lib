<template>
  <div id="app">
    <Container
      width="100%"
      isFlexible="false"
      style="border: 1px solid indianred"
    >
      <Column minSize="25%">aaa </Column>
      <Column minSize="25%" >aaa </Column>
      <Container
        width="50%"
        style="border: 1px solid indianred"
      >
        <Column minSize="25%">aaa </Column>
        <Column minSize="75%" >aaa </Column>
      </Container>
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
