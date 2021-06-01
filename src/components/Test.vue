<template>
  <h1>{{ msg }}</h1>
</template>

<script>
export default {
  props: {
    msg: String
  }
};
</script>

<style lang="scss" scoped>
  h1 {
    color: forestgreen;
  }
</style>
