<template>
    <div :class=baseClass>
        {{ test }}
        <slot />

        <button @click="onClick">
            X
        </button>
    </div>
</template>

<script>
export default {
    props: {
        variant: {
            type: String,
            default: ''
        },
        test: {
            type: String,
            default: 'test'
        }
    },
    computed: {
        baseClass() {
            return [
                'alert',
                this.variant ? `alert-${this.variant}` : ''
            ]
        }
    },
    methods: {
        onClick() {
            console.log('clicou');
            this.$emit('close');
        }
    }
}
</script>

<style scoped>
.alert {
    padding: 5px;
    border-radius: 6px;
    color: gray;
    background: #ddd;
}

.alert-success {
    background: #42b983;
    color: #fff;
}

.alert-danger {
    background: red;
    color: #fff;
}
</style>