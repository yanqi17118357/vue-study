<template>
    <!-- `picked` 在被选择时是字符串 "a" -->
    <input type="radio" v-model="picked" value="a" />

    <!-- `toggle` 只会为 true 或 false -->
    <input type="checkbox" v-model="toggle" />

    <!-- `selected` 在第一项被选中时为字符串 "abc" -->
    <select v-model="selected">
        <option value="abc">ABC</option>
    </select>

</template>

<script>
export default {
    data() {
        return {
            picked: '',
            toggle: '',
            selected: ''
        }
    }
}
</script>

<style scoped>
</style>