<script>
import DishCard from './DishCard.vue'

export default {
    name: "PopularDishes",
    components: {
        DishCard
    },
    data() {
        return {
            dishes: [
                {
                    src: "./src/assets/img/skin-on-fries.jpg",
                    name: "Skin On Fries",
                    price: "$3.00 - $6.00"
                },
                {
                    src: "./src/assets/img/choco-cookie-frappe.jpg",
                    name: "Choco Cookie Frappe",
                    price: "$4.99"
                },
                {
                    src: "./src/assets/img/donut-burger.jpg",
                    name: "The Donut Burger",
                    price: "$6.99"
                }
            ]
        }
    }
}
</script>

<template>
    <section id="popular-dishes">
        <h2>Our Most Popular Dishes</h2>

        <div id="dishes-container">
            <DishCard v-for="(dish, index) in dishes" :key="index" :details="dish" />
        </div>

        <div id="red-button-popular-dishes">
            <a href="#" class="red-button white">START YOUR ORDER <i class="fa-solid fa-circle-right"></i></a>
        </div>

        <div id="main-image-container">
            <img id="main-wave" src="../assets/img/svg-0.svg" alt="main-wave">
            <img id="wave-2" src="../assets/img/svg-0.svg" alt="wave-2">
            <img id="wave-3" src="../assets/img/svg-0.svg" alt="wave-3">
            <img id="wave-4" src="../assets/img/svg-0.svg" alt="wave-4">
        </div>

    </section>
</template>

<style lang="scss">
@use "../styles/partials/mixins.scss" as *;

#popular-dishes {
    margin-top: 100px;
    overflow-x: hidden;

    h2 {
        text-align: center;
        font-size: 40px;
    }

    #dishes-container {
        padding: 70px 20% 50px;
        @include my-flex-row;
        gap: 30px;
    }

    #red-button-popular-dishes {
        display: flex;
        justify-content: center;
    }

    #main-image-container {
        width: 100%;
        height: 500px;
        background-image: url(../assets/img/first-order-background-scaled.jpg);
        background-size: cover;
        background-position: center;
        position: relative;

        #main-wave {
            width: 105%;
            height: 303px;
            position: absolute;
            top: 0;
            left: 0;
        }

        #wave-2 {
            position: absolute;
            width: 110%;
            height: 305px;
            top: 18px;
            left: -22px;
            opacity: 0.2
        }

        #wave-3 {
            position: absolute;
            width: 120%;
            height: 320px;
            top: 45px;
            left: 0;
            opacity: 0.2
        }

        #wave-4 {
            position: absolute;
            width: 115%;
            height: 330px;
            top: 87px;
            left: -80px;
            opacity: 0.2
        }
    }
}
</style>