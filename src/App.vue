<template>
    <p>
        Ask a yes/no question:
        <input v-model="question" />
    </p>
    <p>{{ answer }}</p>

</template>

<script>
export default {
    data() {
        return {
            question: '',
            hh: {name: 'Tom', city: 'Beijing'},
            answer: 'Questions usually contain a question mark. ;-)'
        }
    },
    watch: {
        // 每当 question 改变时，这个函数就会执行
        question(newQuestion, oldQuestion) {
            if (newQuestion.includes('?')) {
                this.getAnswer()
            }
        },
        // 也支持下面这种，可以用.简单的分割对象的键，如果函数不需要参数可以省去function(...)
        'hh.name': function(newQuestion, oldQuestion) {
            if (newQuestion.includes('?')) {
                this.getAnswer()
            }
        }
    },
    methods: {
        async getAnswer() {
            this.answer = 'Thinking...'
            try {
                const res = await fetch('https://yesno.wtf/api')
                this.answer = (await res.json()).answer
            } catch (error) {
                this.answer = 'Error! Could not reach the API. ' + error
            }
        }
    }
}
</script>

<style scoped>
</style>