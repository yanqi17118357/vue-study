<template>
<!--    true-value 和 false-value 是 Vue 特有的 attributes-->
    <input
        type="checkbox"
        v-model="toggle"
        :true-value="dynamicTrueValue"
        :false-value="dynamicFalseValue" />
<!--    复选框未选中是不会向表单提交数据的，单选框会-->
    <input type="radio" v-model="pick" :value="first" />
    <input type="radio" v-model="pick" :value="second" />

</template>

<script>
export default {
    data() {
        return {
            toggle: '',
            dynamicTrueValue: "正确的",
            dynamicFalseValue: "错误的",
            pick: '',
            first: "第一",
            second: "第二"
        }
    }
}
</script>

<style scoped>
</style>