<template>
    <div>
        <p class="text-red">{{ text }}</p>
        <p class="text-green" @click.once="$emit('onTimer')">{{ count }}</p>
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

</style>
