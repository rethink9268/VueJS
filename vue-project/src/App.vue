<template>
  <Greeting :age="age" />
  <age :age="age" @age-change="updateAge"></age>
</template>

<script>
import Greeting from './components/Greeting.vue'
import Age from './components/Age.vue'

export default {
  name: 'App',
  components: {
    Greeting,
    Age
  },
  data() {
    return {
      age: 20
    }
  },
  methods: {
    updateAge(num) {
      this.age += num
    }
  }
}
</script>

