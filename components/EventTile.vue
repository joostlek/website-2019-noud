<template>
  <a class="event-tile container" :href="event.url">
    <h5>{{ toDateString }}</h5>
    <h4>{{ event.title }}</h4>
    <p class="small">{{ event.description }}</p>
  </a>
</template>

<script>
export default {
  name: 'EventTile',
  props: {
    event: {
      type: Object,
      required: true,
    }
  },
  computed: {
    toDateString() {
      const date = new Date(this.event.date * 1000)
      return `${date.getDate()} ${this.getMonthAsString(date.getMonth())} ${date.getFullYear()}`
    },
    getCourseColor() {
      return '#ff00ff'
    }
  },
  methods: {
    getMonthAsString() {
      const monthList = [
        'Januari',
        'Februari',
        'Maart',
        'April',
        'Mei',
        'Juni',
        'Juli',
        'Augustus',
        'September',
        'Oktober',
        'November',
        'December'
      ]
      const currentMonth = new Date().getMonth()

      return monthList[currentMonth]
    }
  }
}
</script>

<style lang='scss' scoped>
.event-tile {
  display: inline-flex;
  min-width: 300px;
  flex: 1;
  flex-direction: column;
  border-top: 4px solid #72c9e1;
  flex-direction: wrap;
  margin: 16px;
  background: #f3f8fa;
  padding: 10px;
  box-shadow: 0 0 20px 0 rgba(0, 0, 0, 0.2);
  transition: box-shadow 300ms;

  &:hover {
    box-shadow: 0 0 20px 0 rgba(0, 0, 0, 0.5);
  }

  h5 {
    color: #72c9e0;
    margin: 0 0 8px 0;
  }

  h4 {
    color: #8d8f91;
    margin: 0;
  }

  p {
    color: #8d8f91;
    margin: 0;
    text-overflow: ellipsis;
  }
}
</style>
