<template>
    <div>
        <!-- <p class="text-green">{{ count }}</p> -->
    </div>
</template>

<script>

    export default {
        name: 'PrintComponent',
        props: {
            count_c: {
                type: Number,
                default: null
            },
        },
        // data() {
        //     return {
        //         text: "Hello World!",
        //         countSecond: 0,
        //         numbers: 0
        //     }
        // },
        // methods: {

        //     multiply: function() {
        //         this.$emit('updateCountSecond', this.count * 2)
        //     },

        // },
        watch: {
            count_c: function(newValue, oldValue) {
                console.log(newValue, oldValue)
                this.$emit('updateCountSecond_c', this.count_c * 2)
            }
        },
        // mounted() {
        // //    this.startTimer( )
        //     this.multiply()
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
