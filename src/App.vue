<!--
Hover your mouse over me for a few seconds to see my dynamically bound title!

This should be red... but click me to toggle it.

This should be green, and should toggle between green and blue on click.
-->

<script>
export default {
    data() {
        return {
            data: "hello, world",
            isRed: true,
            color: 'green'
        }
    },
    methods: {
        redTrans() {
            this.isRed = !this.isRed;
        },
        transColor() {
          this.color = (this.color === "green") ? 'blue' : 'green';
        }
    }

}
</script>

<template>
    <p>
        <span :title="data">
            Hover your mouse over me for a few seconds to see my dynamically bound title!
        </span>
    </p>

    <p :class="{ red: isRed }" @click="redTrans">
        This should be red... but click me to toggle it.
    </p>

    <p :style="{ color }" @click="transColor">
        This should be green, and should toggle between green and blue on click.
    </p>

</template>

<style>
.red {
    color: red;
}
</style>