<template>
    <div>

        <input 
            v-model="inputText" 
            type="text" 
            name="" 
            id=""
            placeholder="Ввести текст"
        />

    </div>
</template>

<script>

    export default {
        name: 'PrintComponent',
        props: {
            text_c: {
                type: String,
                required: true
            }
        },
        data() {
            return {
                inputText: ""
            }
        },
        watch: {
            inputText: function() {
                this.$emit('inputText_c', this.inputText)
            }
        },
        mounted() {
            this.inputText = this.text_c
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
