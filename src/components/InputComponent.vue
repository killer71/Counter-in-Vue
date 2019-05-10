<template>


        <!-- <foto-component
            description="Description for product"
            :price="price"
            v-for="card in cards"
        ></foto-component> -->

        <!-- img(:src="card.img") -->

          <!-- .card__bg(:style="{backgroundImage: `url('${card.img}')` }") -->

    <div>
        <input 
            v-model="inputTextSecond" 
            type="text"
        />

        <p>{{text}}</p>
    </div>
</template>

<script>

    export default {
        name: 'InputComponent',
        props: {
            input_c: {
                type: String,
                required: true
            },
            text: {
                type: String,
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

