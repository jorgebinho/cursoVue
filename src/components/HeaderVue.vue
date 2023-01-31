<template>
    <header class="header">
        <h1 class="title" v-if="$slots.title">
            <slot name="title"/>
        </h1>

        <div class="description">
            <slot name="description"/>
        </div>

        <div class="content">
            <slot />
        </div>
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