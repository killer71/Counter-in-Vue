<template>
    <div>
  
        <input 
            :value="checInput_c"
            @input="$emit('checkbox_c', $event.target.value)"
            type="checkbox"
            class="checkbox"
        
        />

    </div>
</template>

<script>

    export default {
        name: 'CheckboxComponent',
        props: {
            checInput_c: {
                type: Boolean,
                default: null
            },
            value: {
                type: String,
                default: null
            },
        },
        data() {
            return {
                value: "",
            }
        },
        
    }

</script>

<style scoped>

    .checkbox {
        margin-top: 30px;
    }

</style>