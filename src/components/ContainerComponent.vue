<template>
    <div class="border">
        <print-component 
            :count="count"
            @onTimer="startTimer"
        ></print-component>
    </div>   
</template>

<script>
    import PrintComponent from './PrintComponent.vue'
    
    export default {
        name: 'ContainerComponent',
        components: {
            PrintComponent
        },
        data() {
            return {
                count: 0,
            }
        },
        methods: {
            startTimer: function() {
                setInterval(this.countUp, 1000);
            },

            countUp: function() {
                this.count++;
            }
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
