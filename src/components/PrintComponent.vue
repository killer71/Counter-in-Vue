<template>
    <div>
        <p class="text-red">{{ text }}</p>
        <p class="text-green">{{ count }}</p>

        <print-second-component
            @incrementCount="incrementCount"
        ></print-second-component>

        {{ numbers }}

    </div>
</template>

<script>
    import PrintSecondComponent from './PrintSecondComponent.vue'

    export default {
        name: 'PrintComponent',
        components: {
            PrintSecondComponent
        },
        props: {
            count: {
                type: Number,
                default: null
            },
        },
        data() {
            return {
                text: "Hello World!",
                countSecond: 0,
                numbers: 0
            }
        },
        methods: {
            startTimer: function() {
                setInterval(this.countUp, 1000);
            },

            countUp: function() {
                this.$emit('updateCountSecond', this.countSecond++)
            },

            incrementCount: function(numb) {
                this.numbers = numb
            },

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
