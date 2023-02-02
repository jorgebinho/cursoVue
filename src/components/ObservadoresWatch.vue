<template>
    <h2>Observadores</h2>
    <div>
        <input type="text" v-model="name">
        <br>
        {{ name }}

        <br>
        <br>

        <input type="text" v-model="user.first_name">
        <input type="text" v-model="user.last_name">
        <br>
        {{ user.first_name }} {{ user.last_name }}


        <br>
        <br>

        <select v-model="pageCount">
            <option value="5">5</option>
            <option value="10">10</option>
            <option value="15">15</option>
        </select>
        {{ pageCount }}
    </div>
</template>

<script>
export default {
    data() {
        return {
            name: '',
            pageCount: 5,
            user: {
                first_name: '',
                last_name: '',
            }
        }
    },
    watch: {
        name(novoValor, antigoValor) {
            console.log(novoValor, antigoValor);
        },
        pageCount() {
            this.changePage();
        },
        user: {
            handler() {
                console.log('User alterado');
            },
            deep: true
        }
    }, 
    methods: {
        changePage() {
            console.log('Ajax changePage')
        }
    }
}
</script>