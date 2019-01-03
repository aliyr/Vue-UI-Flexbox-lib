<template>
  <div id="app">
    <Container>
      <Col :minSize="200">aaa </Col>
      <Col :>aaa </Col>
      <Col :minSize="300">aaa </Col>
    </Container>
  </div>
</template>

<script>
import Container from './components/Container'
import Col from './components/Col'

export default {
  name: 'app',
  components: {
    Container,
    Col
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
