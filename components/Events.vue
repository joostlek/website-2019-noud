<template>
  <div class="events-container" id="events">
    <h2 class="center">Opkomende activiteiten</h2>

    <div class="events">
      <EventTile v-for="(event, idx) in events" :key="idx" :event="event" />
    </div>
  </div>
</template>

<script>
import EventTile from '../components/EventTile'

export default {
  name: 'Events',
  components: {
    EventTile
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
      },
      {
        title: 'Title',
        description: 'Integer dictum arcu vitae magna pulvinar interdum. Quisque semper arcu sed mauris efficitur pulvinar.',
        date: 1257898,
        url: '#',
        course: 'BIM'
      },
      {
        title: 'Title',
        description: 'Integer dictum arcu vitae magna pulvinar interdum. Quisque semper arcu sed mauris efficitur pulvinar. Integer dictum arcu vitae magna pulvinar interdum. Quisque semper arcu sed mauris efficitur pulvinar.',
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
  })
}
</script>

<style lang="scss">
.events-container {
  max-width: 1084px;
  margin: 0 auto;

  .events {
    display: flex;
    justify-content: space-between;
    flex-direction: row;
    flex-wrap: wrap;

    .event-tile {}
  }

}
</style>
