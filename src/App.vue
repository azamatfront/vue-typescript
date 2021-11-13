<template>
  <div class="app">
    <p>{{ name }} - {{ age }}</p>
		<button @click="changeName('Developer')">Change name</button>
		<button @click="changeAge(27)">Change age</button>
  </div>
</template>

<script lang="ts">

// you can't write inside data() like this instead write (as) keyword inside data()
let age: number | string = 26

import { defineComponent } from "vue";

export default defineComponent({
  name: "App",
  components: {},
  data() {
    return {
      name: "Azamat",
			age: 26 as number | string
    };
  },
  methods: {
    changeName(name: string) {
      this.name = name;
    },
		changeAge(age: number) {
			this.age = age
		}
  },
});
</script>

<style></style>
