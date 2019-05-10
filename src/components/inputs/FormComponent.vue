<template>
    <div>
        <input-component
            :text_c="text_p"
            @inputText_c="inputText_p"
        ></input-component>

        <b>{{text_p}}</b>

        <textarea-component
            :textareaText_c="textareaText_p"
            @textarea_c="textarea_p"
        ></textarea-component>

        <b>{{ textareaText_p }}</b>

    </div>
</template>

<script>
    import InputComponent from './InputComponent.vue'
    import TextareaComponent from './TextareaComponent.vue'

    export default {
        name: 'FormComponent',
        components: {
            InputComponent,
            TextareaComponent
        },
        data() {
            return {
                text_p: "Hello",
                textareaText_p: "It is texarea"
            }
        },
        methods: {
            inputText_p: function(text) {
                this.text_p = text
            },

            textarea_p: function(txt) {
                this.textareaText_p = txt
            },
        },
    }

</script>

<style scoped>

</style>