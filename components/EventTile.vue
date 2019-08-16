<template>
  <div class="main-container">
    <a class="container">
      <h5>{{ toDateString }}</h5>
      <h3>{{ event.title }}</h3>
      <p>{{ event.description }}</p>
    </a>
  </div>
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
a {
  text-decoration: none;
}

.main-container {
  display: inline-block;
}

.container {
  border-top: 5px solid #72c9e1;
  width: 300px;
  height: 175px;
  background: #f3f8fa;
  display: inline-block;
  padding: 10px;
  -webkit-box-shadow: 0 0 20px 0 rgba(0, 0, 0, 0.2);
  -moz-box-shadow: 0 0 20px 0 rgba(0, 0, 0, 0.2);
  box-shadow: 0 0 20px 0 rgba(0, 0, 0, 0.2);
  -webkit-transition: box-shadow 0.3s;
  -moz-transition: box-shadow 0.3s;
  -ms-transition: box-shadow 0.3s;
  -o-transition: box-shadow 0.3s;
  transition: box-shadow 0.3s;
  &:hover {
    -webkit-box-shadow: 0 0 20px 0 rgba(0, 0, 0, 0.5);
    -moz-box-shadow: 0 0 20px 0 rgba(0, 0, 0, 0.5);
    box-shadow: 0 0 20px 0 rgba(0, 0, 0, 0.5);
  }
}

h5 {
  color: #72c9e0;
  margin: 0;
  font-family: 'Roboto Medium', serif;
  font-size: 18px;
  font-weight: normal;
}

h3 {
  color: #8d8f91;
  font-family: 'Roboto Medium', serif;
  font-size: 24px;
  font-weight: normal;
  margin-top: 5px;
  margin-bottom: 0;
}

p {
  color: #8d8f91;
  font-family: Calibri, serif;
  font-size: 18px;
  font-weight: normal;
  margin-top: 5px;
  margin-bottom: 0;
  overflow: hidden;
  -ms-text-overflow: ellipsis;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 5;
  -webkit-box-orient: vertical;
}
</style>
