<template>
  <div v-if="type === 'center'" :class="['text-block', type]">
    <h1>{{ title }}</h1>
    <p>{{ text }}</p>
    <Button v-if="readMoreButtonText !== ''" :onClick="readMoreCallback" size="l">
      {{ readMoreButtonText }}
    </Button>
  </div>

  <div v-else-if="type === 'left-image'" :class="['text-block', type]">
    <div class="left">
      <img :src="image" alt="sponsor logo title" />
    </div>
    <div class="right">
      <h1>{{ title }}</h1>
      <p>{{ text }}</p>
      <Button v-if="readMoreButtonText !== ''" :onClick="readMoreCallback" size="l">
        {{ readMoreButtonText }}
      </Button>
    </div>
  </div>

  <div v-else-if="type === 'right-image'" :class="['text-block', type]">
    <div class="left">
      <h1>{{ title }}</h1>
      <p>{{ text }}</p>
      <Button v-if="readMoreButtonText !== ''" :onClick="readMoreCallback" size="l">
        {{ readMoreButtonText }}
      </Button>
    </div>
    <div class="right">
      <img :src="image" alt="sponsor logo title" />
    </div>
  </div>

  <div v-else class="text-block">
    <h1>{{ title }}</h1>
    <p>{{ text }}</p>
    <Button v-if="readMoreButtonText !== ''" :onClick="readMoreCallback" size="l">
      {{ readMoreButtonText }}
    </Button>
  </div>
</template>

<script>
import Button from './interactions/button'

export default {
  name: 'TextBlock',
  components: { Button },
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
    },
    readMoreCallback: {
      type: Function,
      default: () => {
        console.log('Clicked read more')
      }
    },
    readMoreButtonText: {
      type: String,
      default: ''
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
      width: 100%;
      height: auto;
    }

    .left {
      flex: 1;
    }

    .right {
      flex: 1;
    }
  }
  Button {
    margin-left: auto;
    margin-right: auto;
    display: inherit;
  }
}
</style>
