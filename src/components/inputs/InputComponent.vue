<template>
    <div>
        <input
            :value="text_c"
            @input="$emit('inputText_c', $event.target.value)"
            type="text"
            placeholder="Ввести текст"
        />
    </div>
</template>

<script>

    export default {
        name: 'InputComponent',
        props: {
            text_c: {
                type: String,
                default: null
            },
            value: {
                type: String,
                default: null
            },
        },
        data() {
            return {
                value: ""
            }
        },
    }

</script>

<style scoped>

</style>