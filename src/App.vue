<template>
  <HeaderVue v-show="showHeader"/>

  <DiretivasCondicionais />
  <DiretivasLoop />

</template>

<script>
import HeaderVue from './components/HeaderVue.vue';
import DiretivasCondicionais from './components/DiretivasCondicionais.vue';
import DiretivasLoop from './components/DiretivasLoop.vue';

export default {
    name: 'App',
    components: {
      HeaderVue,
      DiretivasCondicionais,
      DiretivasLoop
    },
    data() {
      return {
        showHeader: true
      }
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