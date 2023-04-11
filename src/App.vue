<template>
<!--    true-value 和 false-value 是 Vue 特有的 attributes-->
    <input
        type="checkbox"
        v-model="toggle"
        true-value="yes"
        false-value="no" />

</template>

<script>
export default {
    data() {
        return {
            toggle: ''
        }
    }
}
</script>

<style scoped>
</style>