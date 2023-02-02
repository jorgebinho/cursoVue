<template>
    <h2>Life Cycle</h2>
    <ul>
        <li>Criação = Preparar o componente | AJAX, incializa algumas variáveis | Não tem acesso ao DOM</li>
        <li>Montagem = Inicializa libs externas | Precisa de acesso ao DOM </li>
        <li>Atualização = Debug | Update</li>
        <li>Desmontagem = Remover tudo que for necessário para liberar memória</li>

    </ul>
    <HeaderVue v-if="showHeader">Life Cycle</HeaderVue>
    <button @click="showHeader = !showHeader">
        Toggle Header
    </button>
    <br>
    <input type="text" v-model="name">
</template>

<script>
import HeaderVue from './HeaderVue.vue';

export default {
    data() {
        return {
            name: "Jorge Almeida",
            showHeader: true
        };
    },
    //HOOKS
    beforeCreate() {
        console.log("beforeCreate");
        console.log("Estado: ", this.name);
        console.log("DOM: ", this.$el);
    },
    created() {
        console.log("created");
        console.log("Estado: ", this.name);
        console.log("DOM: ", this.$el);
    },
    beforeMount() {
        console.log("beforeMount");
        console.log("Estado: ", this.name);
        console.log("DOM: ", this.$el);
    },
    mounted() {
        console.log("mounted");
        console.log("Estado: ", this.name);
        console.log("DOM: ", this.$el);
    },
    beforeUpdate() {
        console.log('beforeUpdate');
    },
    updated() {
        console.log('updated');
    },
    beforeUnmount() {
        console.mount("beforeUnmounted");
        console.log("Estado: ", this.name);
        console.log("DOM: ", this.$el);
    },
    unmounted() {
        console.log("unmounted");
        console.log("Estado: ", this.name);
        console.log("DOM: ", this.$el);
    },
    components: { HeaderVue }
}
</script>