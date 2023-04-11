<template>
<!--    v-model作为selected的数据源-->
    <select v-model="selected">
        <option v-for="option in options" :value="option.value">
            {{ option.text }}
        </option>
    </select>

    <div>Selected: {{ selected }}</div>

</template>

<script>
export default {
    data() {
        return {
            selected: 'A',
            options: [
                { text: 'One', value: 'A' },
                { text: 'Two', value: 'B' },
                { text: 'Three', value: 'C' }
            ]
        }
    }
}
</script>

<style scoped>
</style>