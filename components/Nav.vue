<template>
  <nav class="nav">
    <div class="container flex">
      <div v-if="!isHome" class="logo">
        <n-link to="/">
          <img src="/logo/indicium-logo-left.svg" alt="Indicium Logo" />
        </n-link>
      </div>

      <ul :style="{ margin: isHome ? '0 auto' : '0'}">
        <li v-for="item in items" :key="item.title + item.url">
          <a v-if="item.url.startsWith('http')" :href="item.url">{{ item.title }}</a>
          <n-link v-else :to="item.url" prefetch>
            {{ item.title }}
          </n-link>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Nav',
  data: () => ({
    items: [{
      title: 'Contact',
      url: '#'
    },
    {
      title: 'Partners',
      url: '#'
    },
    {
      title: 'Activiteiten',
      url: '/activiteiten'
    },
    {
      title: 'Commissies',
      url: '#'
    },
    {
      title: 'Lid worden',
      url: '#'
    }]
  }),
  computed: {
    isHome() {
      return this.$route.path === '/'
    }
  }
}
</script>

<style lang="scss" scoped>
.nav {
  opacity: 0.8;
  background: #fff;
  box-shadow: inset 0 -2px 0 0 #cecfcf;

  .logo {
    img {
      max-width: 204px;
    }
  }

  ul {
    list-style: none;
    display: flex;
    max-width: 984px;
    // margin: 0 auto;
    justify-content: space-between;
    align-items: center;
    overflow: auto;

    li {
      a {
        display: block;
        padding: 24px;
        font-size: 16px;
        font-weight: 500;
        color: #8D8F91;
        text-align: center;
        text-decoration: none;
      }
    }
  }
}
</style>
