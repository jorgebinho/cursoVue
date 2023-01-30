<template>
  <HeaderVue v-show="showHeader"/>

  <TwoWayBinding />
  <hr>
  <AtributoClass />
  <hr>
  <DiretivaBinding />
  <hr>
  <DiretivasLoop />
  <hr>
  <DiretivasCondicionais />

</template>

<script>
import HeaderVue from './components/HeaderVue.vue';
import DiretivasCondicionais from './components/DiretivasCondicionais.vue';
import DiretivasLoop from './components/DiretivasLoop.vue';
import DiretivaBinding from './components/DiretivaBinding.vue';
import AtributoClass from './components/AtributoClass.vue';
import TwoWayBinding from './components/TwoWayBinding.vue';

export default {
    name: 'App',
    components: {
      HeaderVue,
      DiretivasCondicionais,
      DiretivasLoop,
      DiretivaBinding,
      AtributoClass,
      TwoWayBinding
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