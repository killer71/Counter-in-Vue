<template>
    <div class="border">
        <print-component text="Hello World!"/>
        <print-component count="0" />
    </div>
   
</template>

<script>
    import PrintComponent from './PrintComponent.vue'
    
    export default {
        name: 'ContainerComponent',
        components: {
            PrintComponent
        },
    }
    
</script>

<style scoped>

    .border {
        border: 1px solid red;
        width: 300px;
        height: 100px;
        margin: auto;
    }
    
</style>
