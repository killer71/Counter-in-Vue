<template>
    <div>
        <input 
            :checked="isChecked_c"
            type="checkbox"
            class="checkbox"
            @change="$emit('checkbox_c', $event.target.checked)"
        />
    </div>
</template>

<script>
    export default {
        name: 'CheckboxComponent',
        props: {
            isChecked_c: {
                type: Boolean,
                default: null
            },
        },
    }
</script>

<style scoped>
    .checkbox {
        margin-top: 30px;
    }
</style>