<template>
  <footer>
    <div class="container">
      <div>
        <h4>Pagina's</h4>
        <ul class="footer-menu pages">
          <li v-for="(menuItem, idx) in menuItems" :key="idx">
            <a :href="menuItem.link">{{ menuItem.title }}</a>
          </li>
        </ul>
      </div>

      <div>
        <h4>Contact</h4>
        <ul class="footer-menu contact">
          <li v-for="(value, key) in contactInfo" :key="key">
            {{ value }}
          </li>
        </ul>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  data: () => ({
    contactInfo: {
      address: 'Heidelberglaan 15',
      postcode: '3584 CS Utrecht',
      lokaal: 'HL15-4.092',
      email: 'bestuur@indicium.hu'
    },
    menuItems: [
      {
        title: 'Inschrijven',
        link: '#'
      },
      {
        title: 'Vacatures',
        link: '#'
      },
      {
        title: 'Statuten',
        link: '#'
      },
      {
        title: 'Over',
        link: '#'
      },
      {
        title: 'Uitleenservice',
        link: '#'
      },
      {
        title: 'Activiteiten',
        link: '#'
      },
      {
        title: 'Sponsoren en partners',
        link: '#'
      },
    ]
  })

}
</script>

<style lang="scss" scoped>
footer {
  background: #DBEFF4;
  padding: 80px;
  color: var(--text-color);

  .container {
    max-width: 1084px;
    margin: 0 auto;
    padding: 0 24px;
    display: flex;
    justify-content: space-between;

    .footer-menu {

      &.pages {
        columns: 2;
      }

      li {
        line-height: 1.6;
      }
    }
  }
}
</style>
