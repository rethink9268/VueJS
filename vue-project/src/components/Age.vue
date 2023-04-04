<template>
  <div>
    <h2>Age: {{ age }}</h2>
    <p>{{ ageDoubled }}</p>
  </div>
  <button @click="onClickAge">Update age</button>
</template>

<script>
export default {
  name: "Age",
  props: {
    age: {
      type: Number,
      required: true,
      default: 20,
      validator(value) {
        return value < 30;
      },
    },
  },
  emits: ["age-change"],
  computed: {
    ageDoubled() {
      return this.age * 2;
    },
  },
  methods: {
    onClickAge() {
      this.$emit("age-change", 1);
    },
  },
};
</script>
