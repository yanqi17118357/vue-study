<template>
    <div>
        <input v-model="question" />
    </div>

</template>

<script>
export default {
    data() {
        return {
            question: ''
        }
    },
    // ...
    watch: {
        question: {
            handler(newQuestion) {
                // 在组件实例创建时会立即调用
                alert("hhh")
            },
            // 强制立即执行回调
            immediate: true
        }
    }
    // ...
}
</script>

<style scoped>
</style>