<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <h1>La mia prima app con Vue CLI!</h1>
    Ciao a tutti
    <p>{{ saluto }}</p>
    <div v-for="(item, index) in test" :key="index">s
      {{ item }}
      <FirstComponent />
    </div>
  </div>
</template>

<script>
import FirstComponent from './components/first-component.vue';
export default {
  name: 'App',
  data() {
    return {
      saluto: `Hello World`,
      test: [1, 4, 8, 12, 15]
    }
  },
  components: {
    FirstComponent,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>