<template>
  <h1>Color Picker Game</h1>

  <div>{{ message }}</div>

  <button v-for="color in colors" :key="color" @click="matchColor(color)">
    {{ color }}
  </button>
</template>

<script>
import composablefile from "../composables/composablefile"
export default {
  name: "ColorPickerGame",
  data() {
    return {
      colors: [],
      message: "",
    };
  },
  methods: {
    matchColor() {},
  },
  setup() {
    const { colors, message, matchColor } = composablefile();
    return { colors, message, matchColor };
  },
};
</script>

<style>
  button {
    padding: 10px 20px;
    margin: 10px;
    border-radius: 5px;
  }
</style>
