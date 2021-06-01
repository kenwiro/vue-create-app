<template>
  <div class="app">
    <div class="greeting">
      <Test
        msg="Create Vue App"
      />
      <h2 class="counter">{{ bar + baz }}</h2>
      <input
        type="button"
        value="Count"
        @click="count"
      >
    </div>
  </div>
</template>

<script>

import foo from './classes/Main';
import Test from './components/Test';

export default {
  components: { Test },
  data() {
    return {
      bar: 1
    };
  },
  computed: {
    baz() {
      return foo(3);
    }
  },
  methods: {
    count() {
      ++this.bar;
    }
  }
};
</script>

<style lang="scss">
  body {
    margin: 0;
    padding: 0;
  }
  .app {
    width: 100%;
    display: flex;
    justify-content: center;
    text-align: center;
  }
  .greeting {
    width: 300px;
  }
  .counter {
    color: cadetblue;
  }
</style>
