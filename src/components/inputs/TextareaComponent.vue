<template>
    <div>
        <textarea
            :value="textareaText_c"
            @input="$emit('textarea_c', $event.target.value)"
            cols="30" 
            rows="3"
        ></textarea>
    </div>
</template>

<script>

    export default {
        name: 'TextareaComponent',
        props: {
            textareaText_c: {
                type: String,
                default: null
            },
            // value: {
            //     type: String,
            //     default: null
            // },
        },
    }

</script>

<style scoped>

</style>