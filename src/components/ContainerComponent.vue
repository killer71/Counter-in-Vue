<template>
    <div class="border">
        <print-component 
            :count_c="count_p"
            @updateCountSecond_c="updateCountSecond_p"
        ></print-component>

        {{ countSecond }}

    </div>   
</template>

<script>
    import PrintComponent from './PrintComponent.vue'
    
    export default {
        name: 'ContainerComponent',
        components: {
            PrintComponent,
        },
        data() {
            return {
                count_p: 0,
                countSecond: 0,
            }
        },
        methods: {
            startTimer: function() {
                setInterval(() => {
                    this.count_p++;
                }, 1000);
            },

            updateCountSecond_p: function(number) {
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
