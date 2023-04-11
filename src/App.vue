<template>
    <input
        :value="text"
        @input="event => text = event.target.value">

    <input v-model="text">

</template>

<script>
export default {
    data() {
        return {
            name: 'Vue.js',
            text: 'hello'
        }
    },
    methods: {
        warn(message, event) {
            // 这里可以访问 DOM 原生事件
            if (event) {
                event.preventDefault()
            }
            alert(message)
        }
    }
}
</script>

<style scoped>
</style>