<template>
  <div class="sponsoren">
    <ul>
      <li v-for="n in 8" :key="n">
        <img src="https://via.placeholder.com/94x63/f2" alt="sponsor logo title" />
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Sponsoren'
}
</script>

<style lang="scss">
.sponsoren {
  padding: 32px 0;
  background: #fff;
  box-shadow: inset 0 -1px 0 0 #C6D1E0, inset 0 1px 0 0 #C6D1E0;

  ul {
    max-width: 1280px;
    margin: 0 auto;
    display: flex;
    overflow: auto;
    justify-content: space-between;
  }
}
</style>
