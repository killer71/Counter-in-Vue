<template>
    <div class="border">
        <print-component
            :text_c="text_p"
            @inputText_c="inputText_p"
        ></print-component>

        <b>{{text_p}}</b>
  
    </div>
</template>

<script>
    import PrintComponent from './PrintComponent.vue'
    
    export default {
        name: 'ContainerComponent',
        components: {
            PrintComponent,
        },
        data() {
            return {
                text_p: "Hello"
            }
        },
        methods: {
            inputText_p: function(txt) {
                this.text_p = txt
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
