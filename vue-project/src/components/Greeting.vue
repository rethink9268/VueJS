<template>
  <div>
    <h1 v-if="age > 25">{{ msg }}</h1>
    <h1 v-else>You must be 25 to see</h1>
  </div>
</template>

<script>
export default {
  name: 'Greeting',
  data() {
    return {
      msg: 'Hi, there!'
    }
  },
  props: ['age']
}
</script>

<style scoped lang="scss">
div {
  h1 {
    color: red;
    cursor: pointer;

    &:hover {
      color: darken(red, 15%);
    }
  }
}
</style>

