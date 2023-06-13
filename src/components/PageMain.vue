<script>
export default {
    name: "PageMain"
}
</script>

<template>
    <!-- Popular Dishes -->
    <section id="popular-dishes">
        <h2>Our Most Popular Dishes</h2>

        <div id="dishes-container">

        </div>

        <div id="red-button-popular-dishes">
            <a href="#" class="red-button white">START YOUR ORDER <i class="fa-solid fa-circle-right"></i></a>
        </div>

    </section>

    <!-- Menu Categories -->
    <section id="menu-categories"></section>

    <!-- Ordering App -->
    <section id="ordering-app"></section>

    <!-- Latest News -->
    <section id="latest-news"></section>
</template>

<style lang="scss">
@use "../styles/partials/mixins.scss" as *;

/* Popular Dishes */
#popular-dishes {
    padding: 0 20%;
    margin-top: 100px;

    h2 {
        text-align: center;
        font-size: 40px;
    }

    #red-button-popular-dishes {
        display: flex;
        justify-content: center;
    }
}

/* Menu Categories */

/* Ordering App */

/* Latest News */
</style>