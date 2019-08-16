<template>
  <div class="main-container">
    <a :href="event.url" class="container">
      <h5>{{ toDateString() }}</h5>
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
      required: true
    }
  },
  methods: {
    toMonthString(month) {
      switch (month) {
        case 0:
          return 'Januari'
        case 1:
          return 'Februari'
        case 2:
          return 'Maart'
        case 3:
          return 'April'
        case 4:
          return 'Mei'
        case 5:
          return 'Juni'
        case 6:
          return 'Juli'
        case 7:
          return 'Augustus'
        case 8:
          return 'September'
        case 9:
          return 'Oktober'
        case 10:
          return 'November'
        case 11:
          return 'December'
        default:
          return 'null'
      }
    },
    toDateString() {
      const date = new Date(this.event.date * 1000)
      return `${date.getDate()} ${this.toMonthString(date.getMonth())} ${date.getFullYear()}`
      // return '9 september 2019'
    },
  }
}
</script>

<style lang="scss" scoped>
  a {
    text-decoration: none;
  }

  .main-container {
    display: inline-block;
  }

  .container {
    border-top: 5px solid #72C9E1;
    width: 300px;
    height: 175px;
    background: #F3F8FA;
    display: inline-block;
    padding: 10px;
    -webkit-box-shadow: 0 0 20px 0 rgba(0, 0, 0, 0.20);
    -moz-box-shadow: 0 0 20px 0 rgba(0, 0, 0, 0.20);
    box-shadow: 0 0 20px 0 rgba(0, 0, 0, 0.20);
    -webkit-transition: box-shadow 0.3s;
    -moz-transition: box-shadow 0.3s;
    -ms-transition: box-shadow 0.3s;
    -o-transition: box-shadow 0.3s;
    transition: box-shadow 0.3s;
    &:hover {
      -webkit-box-shadow: 0 0 20px 0 rgba(0, 0, 0, 0.50);
      -moz-box-shadow: 0 0 20px 0 rgba(0, 0, 0, 0.50);
      box-shadow: 0 0 20px 0 rgba(0, 0, 0, 0.50);
    }
  }

  h5 {
    color: #72C9E0;
    margin: 0;
    font-family: "Roboto Medium", serif;
    font-size: 18px;
    font-weight: normal;
  }

  h3 {
    color: #8D8F91;
    font-family: "Roboto Medium", serif;
    font-size: 24px;
    font-weight: normal;
    margin-top: 5px;
    margin-bottom: 0;
  }

  p {
    color: #8D8F91;
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
