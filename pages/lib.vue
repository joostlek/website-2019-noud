<template>
  <div class="container">
    <Button size="l" :onClick="test">
      Button tekst
    </Button>
    <Button :onClick="test">
      Button tekst
    </Button>
    <Button size="s" :onClick="test">
      Button tekst
    </Button>
    <br /><br />
    <TextLink :callback="test">
      Bekijk agenda
    </TextLink>
    <br />
    <br />
    <br />
    <EventTile v-for="(event, idx) in events" :key="idx" :event="event" />
    <h1>h1 - header</h1>
    <h2>h2 - header</h2>
    <h3>h3 - header</h3>
    <h4>h4 - header</h4>
    <h5>h5 - header</h5>
    <p>
      Aliquam erat volutpat. Curabitur eu ligula nec leo malesuada aliquam. Nulla ut massa vel orci vehicula semper in eu enim. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Vestibulum orci turpis, sagittis ac sem vel, eleifend fermentum lorem. Aenean dignissim metus et dolor aliquet, ut bibendum tellus pulvinar. Pellentesque id risus quis ante pulvinar maximus eget a nulla. Maecenas non erat rutrum, consectetur nibh vel, consectetur mauris. Mauris eget massa risus. Duis malesuada rutrum eros id hendrerit. Sed orci mauris, dignissim non scelerisque in, imperdiet non dui. Praesent eget ligula semper, commodo ipsum non, mattis felis. Proin eget placerat ligula. Vestibulum pellentesque blandit hendrerit.
    </p>
  </div>
</template>

<script>
import Button from '../components/interactions/button'
import EventTile from '../components/EventTile'
import TextLink from '../components/interactions/TextLink'

export default {
  name: 'Lib',
  components: {
    Button,
    EventTile,
    TextLink
  },
  data: () => ({
    events: [
      {
        title: 'Title',
        description: 'Integer dictum arcu vitae magna pulvinar interdum. Quisque semper arcu sed mauris efficitur pulvinar.',
        date: 1257898,
        url: '#',
        course: 'BIM'
      },
      {
        title: 'Title',
        description: 'Integer dictum arcu vitae magna pulvinar interdum. Quisque semper arcu sed mauris efficitur pulvinar.',
        date: 1257898,
        url: '#',
        course: 'SD'
      },
      {
        title: 'Title',
        description: 'Integer dictum arcu vitae magna pulvinar interdum. Quisque semper arcu sed mauris efficitur pulvinar.',
        date: 1257898,
        url: '#',
        course: 'TI'
      }
    ]
  }),
  methods: {
    test() {
      console.log('test')
    }
  }
}
</script>
