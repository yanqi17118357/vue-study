<template>
    <select v-model="selected">
        <!-- 内联对象字面量 -->
<!--        selected 会被设为该对象字面量值 { number: 123 }-->
        <option :value="{ number: 123 }">123</option>
    </select>



</template>

<script>
export default {
    data() {
        return {
            selected: ''
        }
    }
}
</script>

<style scoped>
</style>