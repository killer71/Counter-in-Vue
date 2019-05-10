<template>
    <div>
        <div class="card">
            <img :src="url" class="img" alt="lampa">
            <p class="description">{{ description }}</p>
            <p class="price-old"><strike>{{ oldPrice }}</strike></p>
            <p class="price">{{ price }}</p>
        </div>
    </div>
</template>

<script>

    export default {
        name: 'FotoComponent',
        props: {
            url: {
                type: String,
                default: null
            },
            description: {
                type: String,
                default: null
            },
            oldPrice: {
                type: Number,
                default: null
            },
            price: {
                type: Number,
                default: null
            },
        }
    }

</script>

<style scoped>
    img {
        display: block;
        margin: auto;
    }
    .description {
        display: block;
    }
    .price {
        margin-left: 20px;
        display: inline-block;
        font-size: 24px;
        color: orange;
    }
    .card {
        display: inline-block;
        border: 1px solid tomato;
        width: 300px;
    }

    .price-old {
        display: inline-block;
        color: red;
    }
</style>