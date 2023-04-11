<template>
    <p>Message is: {{ message }}</p>
    <input v-model="message" placeholder="edit me"/>
    <p>Multiline message is:</p>
    <p style="white-space: pre-line;">{{ message }}</p>
    <textarea v-model="message" placeholder="add multiple lines"></textarea>

</template>

<script>
export default {
    data() {
        return {
            message: ' '
        }
    },
    methods: {}
}
</script>

<style scoped>
</style>