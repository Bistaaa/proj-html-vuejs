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

        <div class="add-to-cart">
            <i class="white cart-logo fa-solid fa-cart-shopping"></i>
            <p class="white view-cart">VIEW CART</p>
        </div>
    </div>
</template>

<style lang="scss">
@use "../styles/partials/mixins.scss" as *;

.dish-card {
    width: calc(100% / 3);
    @include my-flex-column;
    gap: 15px;
    align-items: center;
    position: relative;

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

    .add-to-cart {
        position: absolute;
        top: 0;
        left: 0;
        height: 100%;
        width: 100%;
        @include my-flex-column;
        align-items: center;
        justify-content: center;
        transform: translateY(-5%);
        opacity: 0;

        .cart-logo {
            font-size: 30px;
            padding: 25px;
            background-color: rgba(0, 0, 0, 0.8);
            border-radius: 50%;
        }

        .cart-logo:hover {
            color: green;
            cursor: pointer;
        }

        .cart-logo:active {
            transform: scale(0.95);

            .view-cart {
                display: block;
            }
        }

        .view-cart {
            font-size: 13px;
            margin-top: 10px;
            padding: 5px 10px;
            background-color: rgba(0, 0, 0, 0.8);
        }

        .view-cart:hover {
            color: green;
            cursor: pointer;
        }

        .view-cart:active {
            transform: scale(0.95);
        }
    }

    .add-to-cart:hover {
        opacity: 1;
    }

}
</style>