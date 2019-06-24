<template>
  <div id="app">
    <SlottedList :list="list">
      <template v-slot:default="{item}">{{ item.title }} ~ {{ item.subtitle }}</template>
    </SlottedList>
  </div>
</template>

<script>
import SlottedList from "./components/SlottedList";

export default {
  name: "App",
  components: {
    SlottedList
  },
  data: () => ({
    list: [
      { title: "a", subtitle: "b" },
      { title: "a", subtitle: "b" },
      { title: "a", subtitle: "b" },
      { title: "a", subtitle: "b" },
      { title: "a", subtitle: "b" },
      { title: "a", subtitle: "b" }
    ]
  })
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
