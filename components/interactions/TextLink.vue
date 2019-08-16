<template>
  <div @click="callback">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'TextLink',
  props: {
    callback: {
      type: Function,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
  div {
    font-weight: 500;
    font-family: Roboto, serif;
    font-size: 24px;
    line-height: 140%;
    letter-spacing: 1.5px ;
    color: #72C9E0;
    cursor: pointer;
    display: inline-block;
    position: relative;
  }
  div:after {
    position: absolute;
    display: block;
    height: 2px;
    width: 105%;
    border-radius: 1px;
    background-color: #DBEFF4;
    content: '';
    left: -5px;
    bottom: 0;
  }
</style>
