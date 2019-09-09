<template>
  <FullCalendar defaultView="dayGridMonth" :plugins="calendarPlugins" :events="events" />
</template>

<script>
import FullCalendar from '@fullcalendar/vue'
import dayGridPlugin from '@fullcalendar/daygrid'
import axios from 'axios'

export default {
  components: {
    FullCalendar
  },
  data: () => ({
    calendarPlugins: [dayGridPlugin],
    events: []
  }),
  mounted() {
    axios.get('https://indicium.hu/json/events?&filter[start]<2019-10-13&filter[end]=>2019-09-01&page[size]=1000')
      .then((response) => {
        this.mapFetchedEvents(response.data.data)
      })
  },
  methods: {
    mapFetchedEvents(events) {
      const mappedEvents = events.map(event => ({
        id: event.id,
        title: event.attributes.title,
        start: event.attributes.start,
        end: event.attributes.end,
        url: `evenement/${event.attributes.slug}`,
        allday: true
      }))

      this.$set(this, 'events', mappedEvents)
    }
  }
}
</script>

<style lang="scss" scoped>
@import "~/node_modules/@fullcalendar/core/main.css";
@import "~/node_modules/@fullcalendar/daygrid/main.css";
</style>
