<template>
    <div class="border">
        <print-component 
            :count="count"
            @updateCountSecond="updateCountSecond"
        ></print-component>

        {{ countSecond }}

    </div>   
</template>

<script>
    import PrintComponent from './PrintComponent.vue'
    import PrintSecondComponent from './PrintSecondComponent.vue'
    
    export default {
        name: 'ContainerComponent',
        components: {
            PrintComponent,
            PrintSecondComponent
        },
        data() {
            return {
                count: 0,
                countSecond: 0,
            }
        },
        methods: {
            startTimer: function() {
                setInterval(this.countUp, 1000);
            },

            countUp: function() {
                this.count++;
            },

            updateCountSecond: function(number) {
                this.countSecond = number
            },

        },
        mounted() {
            this.startTimer()
        }
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
