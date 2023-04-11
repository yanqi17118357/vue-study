<template>
    <select v-model="selected">
        <!-- 内联对象字面量 -->
<!--        selected 会被设为该对象字面量值 { number: 123 }-->
        <option :value="{ number: 123 }">123</option>
    </select>
    <!-- 在 "change" 事件后同步更新而不是 "input" -->
    <input v-model.lazy="msg" />

<!--    输入自动转换为数字，如果该值无法被 parseFloat() 处理，那么将返回原始值。-->
    <input v-model.number="age" />

<!--    默认自动去除用户输入内容中两端的空格-->
    <input v-model.trim="msg" />

</template>

<script>
export default {
    data() {
        return {
            selected: '',
            msg: '',
            age: ''
        }
    }
}
</script>

<style scoped>
</style>