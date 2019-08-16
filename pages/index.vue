<template>
  <div>
    <Nav />
    <Heading />
    <Sponsoren />
    <TextBlock
      type="center"
      title="Over Indicium"
      text="Wij zijn dé studievereniging voor HBO-ICT van Hogeschool Utrecht. We organiseren het hele jaar door activiteiten zoals bedrijfsbezoeken, kroegcolleges, gastcolleges, lunchlezingen, en nog veel meer over allerlei verschillende onderwerpen. Maar we organiseren natuurlijk ook activiteiten voor gezelligheid! Kom eens langs op onze borrels, LAN-party's of iets anders dat we organiseren!"
    />
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

<style lang="scss">
@import url('https://fonts.googleapis.com/css?family=Roboto:300,400,500,700&display=swap');

* {
  box-sizing: border-box;
}

body {
  font-family: 'Roboto', sans-serif;
}
</style>
