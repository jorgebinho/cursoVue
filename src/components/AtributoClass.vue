<template>
    <h2>Class e Style Dinâmicos</h2>
    <div>
        <h1 :class="{ 'title': true, 'title-home' : isHome }">Curso Vue 3</h1>
        <p :class="['text']"> 
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Alias, totam esse quis ratione ullam deserunt! Quod a, mollitia blanditiis aliquid sit distinctio. Quibusdam perferendis eveniet praesentium incidunt facere molestias fuga.
        </p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            classVar: 'title',
            isHome: true,
            pClass: 'text'
        }
    }
}
</script>

<style>
.title {
    font-size: 20px;
    color: blue;
}

.title-home {
    font-size: 40px;
    color: green;
}

.text {
    color: gray;
}
</style>