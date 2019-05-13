<template>
    <div>
       <select class="select" value="selected_c" @change="$emit('sel_c', $event.target.value)">
            <option value="" selected="selected">Виберіть опцію ...</option>
            <option v-for="option in options">{{ option }}</option>
       </select>
    </div>
</template>

<script>
    export default {
        name: 'SelectComponent',
        props: {
            // option: {
            //     type: Array,
            //     default: null
            // },
            selected_c: {
                type: String,
                default: null
            },
            // value: {
            //     type: String,
            //     default: null
            // },
        },
        data() {
            return {
                options: ["One", "Two", "Three", "Four"],
            }
        }
    }
</script>

<style scoped>
    .select {
        margin-top: 50px;
        width: 200px;
    }
</style>