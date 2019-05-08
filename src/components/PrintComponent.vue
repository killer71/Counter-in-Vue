<template>
    <div>
        <p class="text-red">{{ text }}</p>
        <p class="text-green" @click.once="$emit('onTimer')">{{ count }}</p>
        <p class="text-orange" @click.once="startTimer">{{ countSecond }}</p>
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
                this.countSecond++;
            }
        },
        // methods: {
        //     startTimer() {
        //         this.$emit('onTimer')
        //     },
        // },
    }
    
</script>

<style scoped>

    .text-red {
        color: red;
    }

    .text-green {
        color: green;
    }

    .text-orange {
        color: orange;
    }

</style>
