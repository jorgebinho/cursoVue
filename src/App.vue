<template>
  <HeaderVue>
    <template v-slot:title>
      Home
    </template>

    <template v-slot:description>
      <p>Descrição</p>
    </template>

    Conteúdo adicional do Header...
  </HeaderVue>

  <BaseCard />
  <hr>
  <LifeCycle />
  <hr>
  <ObservadoresWatch />
  <hr>
  <ComputedProperties />
  <hr>
  <EventosVue />
  <hr>
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
import EventosVue from './components/EventosVue.vue';
import ComputedProperties from './components/ComputedProperties.vue';
import ObservadoresWatch from './components/ObservadoresWatch.vue';
import LifeCycle from './components/LifeCycle.vue';
import BaseCard from './components/BaseCard.vue';

export default {
    name: 'App',
    components: {
      HeaderVue,
      DiretivasCondicionais,
      DiretivasLoop,
      DiretivaBinding,
      AtributoClass,
      TwoWayBinding,
      EventosVue,
      ComputedProperties,
      ObservadoresWatch,
      LifeCycle,
      BaseCard
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