<template>
  <div class="container">
    <Button size="l">Button tekst</Button>
    <Button>Button tekst</Button>
    <Button size="s">Button tekst</Button>
    <br /><br/>

    <EventTile v-for="(event, idx) in events" :event="event" :key="idx" />
  </div>
</template>

<script>
import Button from '../components/interactions/button'
import EventTile from '../components/EventTile'

export default {
  name: 'Lib',
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
  components: {
    Button,
    EventTile
  }
}
</script>
