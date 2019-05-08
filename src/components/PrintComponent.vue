<template>
    <div>
        <p class="text-red">{{ text }}</p>
        <p class="text-green">{{ count }}</p>
    </div>
</template>

<script>

    export default {
        name: 'PrintComponent',
        props: {
            count: {
                type: Number,
                default: null
            },
        },
        data() {
            return {
                text: "Hello World!",
                countSecond: 0
            }
        },
        methods: {
            startTimer: function() {
                setInterval(this.countUp, 1000);
            },

            countUp: function() {
                this.$emit('updateCountSecond', this.countSecond++)
            }
        },
        mounted() {
            this.startTimer()
        }

    }
    
</script>

<style scoped>

    .text-red {
        color: red;
    }

    .text-green {
        color: green;
    }

</style>
