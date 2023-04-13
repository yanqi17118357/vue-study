<script>
export default {
    data() {
        return {
            list: [
                "1",
                "2"
            ]
        }
    },
    mounted() {
        // 输出所有对应引用的 DOM 元素
        console.log(this.$refs.items)
    }
}
</script>

<template>
    <ul>
        <li v-for="item in list" ref="items">
            {{ item }}
        </li>
    </ul>
</template>

<style scoped>
</style>