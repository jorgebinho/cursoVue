<template>
    <h2>Two Way Data Binding</h2>
    <div>
        <label>Nome</label>
        <input type="text" v-model="name">
        {{ name }}

        <br>
        <br>

        <label>Esportes</label>
        <select v-model="esportes">
            <option value="">Escolha</option>
            <option value="futebol">Futebol</option>
            <option value="skate">Skate</option>
            <option value="tenis">Tênis</option>
        </select>
        {{ esportes }}

        <br>
        <br>

        <label>Newsletter</label>
        <input type="radio" v-model="newsletter" value="Sim">Sim
        <input type="radio" v-model="newsletter" value="Não">Não
        {{ newsletter }}

        <br>
        <br>

        <label>Contrato</label>
        <input type="checkbox" v-model="contrato">Aceita os nossos termos...
        <br>
        {{ contrato }}

        <br>
        <br>

        <label>Cores que você mais gosta</label>
        <input type="checkbox" v-model="cores" value="Azul">Azul
        <input type="checkbox" v-model="cores" value="Amarelo">Amarelo
        <br>
        {{  cores }}
    </div>
</template>

<script>
export default {
    data() {
        return {
            name: "Jorge Almeida",
            esportes: 'futebol',
            newsletter: 'Não',
            contrato: false,
            cores: []
        }
    }
}
</script>

<style>

</style>