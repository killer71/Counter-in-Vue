<template>
    <div>
        <foto-component 
            v-for="card in cards"
            :card="card"
        ></foto-component>
    </div>
</template>

<script>
    import FotoComponent from './FotoComponent.vue'
    
    export default {
        name: 'GalleryComponent',
        components: {
            FotoComponent,
        },
        data() {
            return {
                cards: [
					{
						url: "https://ikea-market.com.ua/uploads/product/medium/lampa-biurkowa-bia-y-tertial-1.jpg",
						description: "Description for First product",
                        oldPrice: 110,
                        price: 100
                    },
                    {
						url: "https://ikea-market.com.ua/uploads/product/medium/sza-umyw-bla-45x45-umyw-bia-y-bia-y-godmorgon-tolken-t-rnviken-1.jpg",
						description: "Description for Second product",
                        oldPrice: 215,
                        price: 200
                    },
                    {
						url: "https://ikea-market.com.ua/uploads/product/medium/lampa-rabochaya-chernyi-lagra-1.jpg",
						description: "Description for Third product",
                        oldPrice: 379,
                        price: 300
					},
                ]
            }
        },
    }

</script>

<style scoped>

</style>