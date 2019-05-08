<template>

</template>

<script>

    export default {
        name: 'PrintSecondComponent',
        data() {
            return {
                numbers: 0
            }
        },
        methods: {
            startTimer: function() {
                setInterval(this.countUp, 2000);
            },

            countUp: function() {
                this.$emit('incrementCount', this.numbers += 5)
            }
        },
        mounted() {
            this.startTimer()
        },
    }

</script>

<style scoped>

</style>