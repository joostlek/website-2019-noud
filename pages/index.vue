<template>
  <div>
    <Nav />
    <Heading />
    <Sponsoren />
    <TextBlock center />
    <Events />
    <TextBlock />
    <TextBlock />
    <TextBlock inverted />
    <Footer />
  </div>
</template>

<script>
import Nav from '../components/Nav'
import Heading from '../components/Heading'
import Footer from '../components/Footer'
import Sponsoren from '../components/Sponsoren'
import TextBlock from '../components/TextBlock'
import Events from '../components/Events'

export default {
  name: 'Home',
  components: {
    Nav,
    Heading,
    Sponsoren,
    TextBlock,
    Events,
    Footer
  }
}
</script>

<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css?family=Roboto:300,400,500,700&display=swap');
body {
  background-color: #72c9e0;
  font-family: 'Roboto', sans-serif;
}
</style>
