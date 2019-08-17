<template>
  <div class="events-container" id="events">
    <h2 class="center">Opkomende activiteiten</h2>

    <div class="categories">
      <ul>
        <li v-for="(category, idx) in allCategories" :key="idx">
          <span :style="{backgroundColor: `#${category.hex}`}"></span>{{ category.courseTitle }}
        </li>
      </ul>
    </div>

    <div class="events">
      <EventTile v-for="(event, idx) in events" :key="idx" :event="event" :allCategories="allCategories" />
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
        categories: ['AI']
      },
      {
        title: 'Title',
        description: 'Integer dictum arcu vitae magna pulvinar interdum. Quisque semper arcu sed mauris efficitur pulvinar.',
        date: 1257898,
        url: '#',
        categories: ['SD', 'BIM']
      },
      {
        title: 'Title',
        description: 'Integer dictum arcu vitae magna pulvinar interdum. Quisque semper arcu sed mauris efficitur pulvinar.',
        date: 1565961457,
        url: '#',
        categories: ['TI']
      },
      {
        title: 'Title',
        description: 'Integer dictum arcu vitae magna pulvinar interdum. Quisque semper arcu sed mauris efficitur pulvinar.',
        date: 12578989,
        url: '#',
        categories: ['SD', 'TI', 'SNE', 'BIM', 'AI']
      },
      {
        title: 'Title',
        description: 'Integer dictum arcu vitae magna pulvinar interdum. Quisque semper arcu sed mauris efficitur pulvinar. Integer dictum arcu vitae magna pulvinar interdum. Quisque semper arcu sed mauris efficitur pulvinar.',
        date: 1257898,
        url: '#',
        categories: ['SD']
      },
      {
        title: 'Title',
        description: 'Integer dictum arcu vitae magna pulvinar interdum. Quisque semper arcu sed mauris efficitur pulvinar.',
        date: 1257898,
        url: '#',
        categories: ['TI', 'SD', 'AI']
      }
    ],
    allCategories: [
      {
        courseTitle: 'SD',
        hex: 'E17272'
      },
      {
        courseTitle: 'TI',
        hex: 'A2E172'
      },
      {
        courseTitle: 'SNE',
        hex: 'E1DB72'
      },
      {
        courseTitle: 'BIM',
        hex: '727AE1'
      },
      {
        courseTitle: 'AI',
        hex: '72E1AD'
      },
    ]
  })
}
</script>

<style lang="scss">
.events-container {
  max-width: 1084px;
  margin: 0 auto;

  .categories {
    ul {
      display: flex;
      justify-content: center;

      li {
        display: inline-flex;
        align-items: center;
        padding: 16px;

        span {
          display: inline-flex;
          width: 24px;
          height: 24px;
          background-color: #f2f2f2;
          margin-right: 8px;
        }
      }
    }
  }

  .events {
    display: flex;
    justify-content: space-between;
    flex-direction: row;
    flex-wrap: wrap;
  }

}
</style>
