<template>
  <button :class="['btn', size]" @click="onClick">
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: 'Button',
  props: {
    onClick: {
      type: Function,
      required: true,
    },
    size: {
      type: String,
      required: false,
      default: 'l'
    }
  }
}
</script>

<style lang="scss" scoped>
  .btn {
    font-family: Roboto, sans-serif;
    color: #fff;
    background: #72c9e0;
    box-shadow: 0 0 32px rgba(181, 187, 201, 0.4);
    border-radius: 4px;
    border: 0;

    &.s {
      padding: 8px;
      font-size: .6rem;
    }

    &.m {
      padding: 8px 12px;
      font-size: .8rem;
    }

    &.l {
      padding: 12px 16px;
      font-size: 1rem;
    }

    &:hover {
      -webkit-box-shadow: 0 0 32px rgba(181, 187, 201, 0.8);
      -moz-box-shadow: 0 0 32px rgba(181, 187, 201, 0.8);
      box-shadow: 0 0 32px rgba(181, 187, 201, 0.8);
    }
  }
</style>
