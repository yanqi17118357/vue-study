<template>
    <div>
        <h2>{{ fullName }}</h2>
        <p>名字：<input v-model="firstName"></p>
        <p>姓氏：<input v-model="lastName"></p>
    </div>

</template>

<script>
export default {
    data() {
        return {
            firstName: '',
            lastName: '',
            fullName: ''
        }
    },
    watch: {
        firstName: {
            handler(newVal, oldVal) {
                this.fullName = newVal + ' ' + this.lastName;
            },
            deep: true
        },
        lastName: {
            handler(newVal, oldVal) {
                this.fullName = this.firstName + ' ' + newVal;
            },
            deep: true
        }
    }
};
</script>

<style scoped>
</style>