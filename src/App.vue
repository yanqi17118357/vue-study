<template>
    <div>
        <p>计数器：{{ count }}</p>
        <button @click="increment">增加</button>
    </div>

</template>

<script>
export default {
    data() {
        return {
            count: 0
        }
    },
    // mounted 钩子可以用来在组件完成初始渲染并创建 DOM 节点后运行代码
    mounted() {
        this.$watch('count', (newVal, oldVal) => {
            console.log(`计数器的值从 ${oldVal} 变为了 ${newVal}`);
        });
    },
    methods: {
        increment() {
            this.count++;
        }
    }
};
</script>

<style scoped>
</style>