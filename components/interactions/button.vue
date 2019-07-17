<template>
  <button @click="onClick">
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
    }
  }
}
</script>

<style lang="scss" scoped>
  button {
    font-family: Roboto,serif;
    font-style: normal;
    font-weight: normal;
    font-size: 24px;
    line-height: 28px;
    align-items: center;
    text-align: center;
    letter-spacing: 0.75px;
    color: #FFFFFF;
    background: #72c9e0;
    -webkit-box-shadow: 0 0 32px rgba(181, 187, 201, 0.4);
    -moz-box-shadow: 0 0 32px rgba(181, 187, 201, 0.4);
    box-shadow: 0 0 32px rgba(181, 187, 201, 0.4);
    -webkit-border-radius: 4px;
    -moz-border-radius: 4px;
    border-radius: 4px;
    border: 0;
    min-width: 200px;
    min-height: 60px;
    padding: 15px;

    &:hover {
      -webkit-box-shadow: 0 0 32px rgba(181, 187, 201, 0.8);
      -moz-box-shadow: 0 0 32px rgba(181, 187, 201, 0.8);
      box-shadow: 0 0 32px rgba(181, 187, 201, 0.8);
    }
  }
</style>
