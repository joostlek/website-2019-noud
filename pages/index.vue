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
    <TextBlock
      type="left-image"
      title="Introkamp"
      text="Sta je op het punt om HBO-ICT te gaan studeren? Dan is ons introkamp de ideale start vóór jouw studie! Ontmoet in vier dagen gelijk al je medestudenten door Utrecht te verkennen, kennis te maken met verschillende partners en een leuk programma georganiseerd door onze introcommissie. Het introkamp voor collegejaar 2019-2020 is van 24 augustus t/m 27 augustus. "
      image="https://indicium.hu/thumbs/800x800r/introkamp/intro-home.png"
      readMoreButtonText="Meld je nu aan!"
    />
    <TextBlock
      type="center"
      title="Lid worden is meedoen!"
      text="Een hoop activiteiten organiseren we voor iedereen. Maar als lid krijg je natuurlijk veel meer voordelen! Je krijgt dan korting bij activiteiten, wordt ook uitgenodigd voor activiteiten die exclusief voor leden zijn, kan reageren op vacatures voor onder andere stages en kun je meebouwen aan de vereniging. "
      readMoreButtonText="Word lid"
    />
    <TextBlock
      type="right-image"
      title="Commissie of bestuur?"
      text="Lijkt het je leuk om je een jaar lang naast je studie keihard in te zetten voor de vereniging? We zijn op zoek naar een nieuw bestuur! Als bestuur ben je het gezicht van de vereniging en bepaal je welke kant de vereniging opgaat het komende collegejaar. Tijdens een bestuursjaar leer je een hoop en ontmoet je heel veel enthousiaste mensen. Wil je meer weten? "
      image="https://indicium.hu/thumbs/800x800r/2019-03/dsc-5016.jpg"
      readMoreButtonText="Lees meer"
    />
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
