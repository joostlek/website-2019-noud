<template>
  <div>
    <h1>Page</h1>

    {{ $data }}
  </div>
</template>

<script>
/* eslint-disable */
export default {
  async asyncData ({ params, error, payload }) {
    console.log({ params, error, payload })
    return { page: payload }
  },
  mounted() {
    console.log('_page')
  }
}
</script>
