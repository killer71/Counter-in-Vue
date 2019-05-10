<template>
    <div>
        <div class="card">
            <img :src="card.url" class="img" alt="lampa">
            <p class="description">{{ card.description }}</p>
            <p class="price-old"><strike>{{ card.oldPrice }}</strike></p>
            <p class="price">{{ card.price }}</p>
        </div>
    </div>
</template>

<script>

    export default {
        name: 'FotoComponent',
        props: {
            card: {
                type: Object,
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