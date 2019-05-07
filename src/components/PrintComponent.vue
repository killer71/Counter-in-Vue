<template>
    <div>
        <p class="text-red">{{ text }}</p>
        <p class="text-green" v-on:click.once="startTimer">{{ count }}</p>
    </div>
</template>

<script>

    export default {
        name: 'PrintComponent',
        props: {
            text: String,
            count: Number
        },
        data: function() {
            return {
                count: 0,
                timer: null
            }
        },
        methods: {
            startTimer: function() {
                this.timer = setInterval(this.countUp, 1000);
            },

            countUp: function() {
                this.count++;
            }
        },
        // computed: {
        //     startTimer: function() {
        //         this.timer = setInterval(this.countUp, 1000);
        //     },
        //     countUp: function() {
        //         this.count++;
        //     }
        // }
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
