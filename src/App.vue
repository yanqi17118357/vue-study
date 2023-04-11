<template>
<!--    true-value 和 false-value 是 Vue 特有的 attributes-->
    <input
        type="checkbox"
        v-model="toggle"
        :true-value="dynamicTrueValue"
        :false-value="dynamicFalseValue" />

</template>

<script>
export default {
    data() {
        return {
            toggle: '',
            dynamicTrueValue: "正确的",
            dynamicFalseValue: "错误的"
        }
    }
}
</script>

<style scoped>
</style>