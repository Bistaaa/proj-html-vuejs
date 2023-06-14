<script>
export default {
    name: "DishCard",
    props: {
        details: Object
    }
}
</script>

<template>
    <div class="dish-card">
        <img class="dish-img" :src="details.src">
        <p class="dish-name">{{ details.name }}</p>
        <p class="dish-price">{{ details.price }}</p>
    </div>
</template>

<style lang="scss">
@use "../styles/partials/mixins.scss" as *;

.dish-card {
    width: calc(100% / 3);
    @include my-flex-column;
    gap: 15px;
    align-items: center;

    .dish-img {
        width: 100%;
    }

    .dish-name {
        font-size: 30px;
        font-weight: bold;
        color: rgba(37, 42, 51, 255);
    }

    .dish-price {
        font-size: 16px;
        color: red;
    }
}
</style>