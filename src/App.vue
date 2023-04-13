<script>
export default {
    // 在Vue组件生命周期的 mounted 钩子函数里，
    // 我们可以确保模板引用所对应的DOM元素已经被创建，可以安全地访问它们了。
    mounted() {
        this.$refs.input.focus()
    }
}
</script>

<template>
<!--    vue在组件挂载后才能访问模板引用-->
    <input ref="input" />
</template>

<style scoped>
</style>