<template>
  <HeaderVue v-show="showHeader"/>

  <div v-show="showName">
    Nome: {{ firstName }} <br>
    Sobrenome: {{ lastName }}
  </div>

  <div v-if="accesLevel === 'adm'">Admin</div>
  <div v-else-if="accesLevel === 'mkt'">Marketing</div>
  <div v-else>User</div>


</template>

<script>
import HeaderVue from './components/HeaderVue.vue';

export default {
    name: 'App',
    components: {
      HeaderVue
    },
    data() {
      return {
        showHeader: true,
        showName: true,
        firstName:  'Jorge',
        lastName: 'Santos',
        accesLevel: 'user'
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