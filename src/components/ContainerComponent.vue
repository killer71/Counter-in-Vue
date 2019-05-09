<template>
    <div class="border">
        <print-component
            :text_c="text_p"
            @inputText_c="inputText_p"
        ></print-component>

        <b>{{text_p}}</b>

        <input-component
            :input_c="input_p"
            @inputSecond_c="inputSecond_p"
        ></input-component>
  
        <b>{{input_p}}</b>

    </div>
</template>

<script>
    import PrintComponent from './PrintComponent.vue'
    import InputComponent from './InputComponent.vue'
    
    export default {
        name: 'ContainerComponent',
        components: {
            PrintComponent,
            InputComponent
        },
        data() {
            return {
                text_p: "Hello",
                input_p: "World"
            }
        },
        methods: {
            inputText_p: function(txt) {
                this.text_p = txt
            },

            inputSecond_p: function(text) {
                this.input_p = text
            }
        },
    }    
</script>

<style scoped>

    .border {
        border: 1px solid red;
        width: 500px;
        height: 200px;
        margin: auto;
    }
    
</style>
