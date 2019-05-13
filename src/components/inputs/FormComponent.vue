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

        <checkbox-component
            :isChecked_c="isChecked_p"
            @checkbox_c="checkbox_p"
        ></checkbox-component>

        <b>{{ isChecked_p }}</b>

        <select-component
           :selected_c="selected_p"
           @sel_c="sel_p"
        ></select-component>
        
        
        <b>{{selected_p}}</b>

    </div>
</template>

<script>
    import InputComponent from './InputComponent.vue'
    import TextareaComponent from './TextareaComponent.vue'
    import CheckboxComponent from './CheckboxComponent.vue'
    import SelectComponent from './SelectComponent.vue'

    export default {
        name: 'FormComponent',
        components: {
            InputComponent,
            TextareaComponent,
            CheckboxComponent,
            SelectComponent
        },
        data() {
            return {
                text_p: "Hello",
                textareaText_p: "It is texarea",
                isChecked_p: true,
                selected_p: ""
                // options: ["One", "Two", "Three", "Four"],
            }
        },
        methods: {
            inputText_p: function(text) {
                this.text_p = text
            },
            textarea_p: function(txt) {
                this.textareaText_p = txt
            },
            checkbox_p: function(check) {
                this.isChecked_p = check
            },
            sel_p: function(select) {
                this.selected_p = select
            }
        },
    }
</script>

<style scoped>

</style>