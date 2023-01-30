<template>
    <h2>Eventos</h2>

    <div>
        <!-- v-on = @ -->
        <button @click="onClick">
            Enviar
        </button>
        <p @mouseover="onMouseOver" @mouseout="onMouseOut">Passe o mouse</p>

        <form action="https://google.com" @submit.prevent="onSubmit">
            <input type="text" @keyup.enter="onKeyUp">
            <button type="submit">Enviar dados</button>
        </form>
    </div>
</template>

<script>
export default {
    methods: {
        onClick($evt) {
            console.log($evt);
        },
        onMouseOver($evt) {
            console.log('mouse over', $evt);
        },
        onMouseOut($evt) {
            console.log('mouse out', $evt);
        }, 
        onSubmit($evt   ) {
            console.log('submit', $evt);
        },
        onKeyUp($evt) {
            console.log('onKeyUp', $evt)
        }
    }
}
</script>