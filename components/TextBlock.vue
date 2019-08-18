<template>
  <div v-if="type === 'center'" :class="['text-block', type]">
    <h1>{{ title }}</h1>
    <p>{{ text }}</p>
  </div>

  <div v-else-if="type === 'left-image'" :class="['text-block', type]">
    <div class="left">
      <img :src="image" alt="sponsor logo title" />
    </div>
    <div class="right">
      <h1>{{ title }}</h1>
      <p>{{ text }}</p>
    </div>
  </div>

  <div v-else-if="type === 'right-image'" :class="['text-block', type]">
    <div class="left">
      <h1>{{ title }}</h1>
      <p>{{ text }}</p>
    </div>
    <div class="right">
      <img :src="image" alt="sponsor logo title" />
    </div>
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
    },
    image: {
      type: String,
      default: 'https://via.placeholder.com/348x408/f2'
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

  &.left-image, &.right-image {
    display: flex;
    img {
      padding: 32px;
      width: auto;
      height: 100%;
    }

    .left {
      flex: 1;
    }

    .right {
      flex: 1;
    }
  }
}
</style>
