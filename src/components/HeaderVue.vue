<template>
    <header class="header">
        Header
    </header>
</template>

<script>
export default {
    beforeUnmount() {
        console.log('beforeUnmount');
    },
    unmounted() {
        console.log('unmounted');
    }
}
</script>

<style>
    .header {
        background: #000;
        color: #fff
    }
</style>