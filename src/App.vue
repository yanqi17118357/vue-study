<template>
    <button @click="show = !show">转换列表显示</button>
    <button @click="list.push(list.length + 1)">插入一条数据</button>
    <button @click="list.pop()">删除一条数据</button>
    <button @click="list.reverse()">反转列表</button>

    <ul v-if="show && list.length">
        <li v-for="item in list">
            {{ item }}
        </li>
    </ul>
    <p v-else-if="list.length">存在列表，但是隐藏了</p>
    <p v-else>列表没有数据</p>
</template>

<script>
export default {
    data() {
        return {
            show: true,
            list: [1, 2, 3]
        }
    }
}
</script>
