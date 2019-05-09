<template>
    <div>
        <input 
            v-model="inputTextSecond" 
            type="text"
        />
    </div>
</template>

<script>

    export default {
        name: 'InputComponent',
        props: {
            input_c: {
                type: String,
                required: true
            }
        },
        data() {
            return {
                inputTextSecond: ""
            }
        },
        watch: {
            inputTextSecond: function() {
                this.$emit('inputSecond_c', this.inputTextSecond)
            }
        },
        mounted() {
            this.inputTextSecond = this.input_c
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

