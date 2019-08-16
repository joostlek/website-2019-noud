<template>
  <nav class="nav">
    <ul>
      <li v-for="item in items" :key="item.title + item.url">
        <a :href="item.url">{{ item.title }}</a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'Nav',
  data: () => ({
    items: [
      {
        title: 'Contact',
        url: '#'
      },
      {
        title: 'Partners',
        url: '#'
      },
      {
        title: 'Agenda',
        url: '#'
      },
      {
        title: 'Commissies',
        url: '#'
      },
      {
        title: 'Lid worden',
        url: '#'
      },
    ]
  })
}
</script>

<style lang="scss" scoped>
.nav {
  opacity: 0.8;
  background: #fff;
  box-shadow: inset 0 -2px 0 0 #cecfcf;

  ul {
    list-style: none;
    display: flex;
    max-width: 1184px;
    margin: 0 auto;
    justify-content: space-between;

    li {
      a {
        display: block;
        padding: 24px;
        font-size: 24px;
        font-weight: 500;
        color: #8D8F91;
        text-align: center;
        text-decoration: none;
      }
    }
  }
}
</style>
