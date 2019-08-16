<template>
  <div v-if="type === 'center'" :class="['text-block', type]">
    <h1>{{ title }}</h1>
    <p>{{ text }}</p>
  </div>
  <div v-else>
    give content
  </div>
</template>

<script>
export default {
  name: 'TextBlock',
  props: {
    type: {
      type: String,
      default: 'center'
    },
    title: {
      type: String,
      default: 'title'
    },
    text: {
      type: String,
      default: 'text'
    }
  }
}
</script>

<style lang="scss">
.text-block {
  max-width: 829px;
  margin: 0 auto;

  &.center {
    text-align: center;
  }
}
</style>
