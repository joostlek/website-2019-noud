<template>
  <div v-if="type === 'center'" :class="['text-block', type]">
    <h1>{{ title }}</h1>
    <p>{{ text }}</p>
  </div>

  <div v-else-if="type === 'left-image'" :class="['text-block', type]">
    left image
  </div>

  <div v-else-if="type === 'right-image'" :class="['text-block', type]">
    right image
  </div>

  <div v-else class="text-block">
    <h1>{{ title }}</h1>
    <p>{{ text }}</p>
  </div>
</template>

<script>
export default {
  name: 'TextBlock',
  props: {
    type: {
      type: String,
      default: ''
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
  padding: 96px 0;

  &.center {
    text-align: center;
  }

  &.right-image {}

  &.left-image {}
}
</style>
