<script>
import CategoryCard from './CategoryCard.vue'

export default {
    name: "MenuCategories",
    components: {
        CategoryCard
    },
    data() {
        return {
            categories: [
                {
                    src: "./src/assets/img/appetizers-menu-background.jpg",
                    name: "APPETIZERS",
                },
                {
                    src: "./src/assets/img/burgers-menu-background.jpg",
                    name: "BURGERS",
                },
                {
                    src: "./src/assets/img/pizza-menu-background.jpg",
                    name: "PIZZAS",
                },
                {
                    src: "./src/assets/img/fries-menu-background.jpg",
                    name: "FRIERS",
                },
                {
                    src: "./src/assets/img/sides-menu-background.jpg",
                    name: "SIDES",
                },
                {
                    src: "./src/assets/img/desserts-menu-background.jpg",
                    name: "DESSERTS",
                },
                {
                    src: "./src/assets/img/beverages-menu-background.jpg",
                    name: "BEVERAGES",
                },
                {
                    src: "./src/assets/img/specials-menu-background.jpg",
                    name: "SPECIALS",
                }
            ]
        }
    }
}
</script>

<template>
    <section id="menu-categories">
        <h2>Menu Categories</h2>

        <button id="view-menu" class="red-button">VIEW THE FULL MENU <i class="fa-solid fa-circle-right"></i></button>

        <div id="menu-categories-container">
            <CategoryCard v-for="(category, index) in categories" :key="index" :info="category" />
        </div>

        <div id="icons-container">
            <div class="icon-column" id="vegetarian">
                <i id="vegetarian-icon" class="icon fa-solid fa-leaf"></i>
                <p class="icon-class">Vegetarian</p>
            </div>
            <div class="icon-column" id="gluten-free">
                <i id="gluten-free-icon" class="icon fa-solid fa-wheat-awn"></i>
                <p class="icon-class">Gluten-Free</p>
            </div>
            <div class="icon-column" id="daity-free">
                <i id="daity-free-icon" class="icon fa-solid fa-glass-water"></i>
                <p class="icon-class">Daity Free</p>
            </div>
            <div class="icon-column" id="keto-friendly">
                <i id="keto-friendly-icon" class="icon fa-solid fa-drumstick-bite"></i>
                <p class="icon-class">Keto Friendly</p>
            </div>
        </div>
    </section>
</template>

<style lang="scss">
@use "../styles/partials/mixins.scss" as *;

#menu-categories {
    padding: 150px 20%;
    position: relative;

    h2 {
        font-size: 40px;
    }

    #view-menu {
        position: absolute;
        right: 20%;
        top: 130px;
    }

    #menu-categories-container {
        @include my-flex-row;
        flex-wrap: wrap;
        gap: 20px
    }

    #icons-container {
        @include my-flex-row;

        .icon-column {
            width: calc(100% / 4);
            @include my-flex-column;
            gap: 20px;
            align-items: center;

            .icon-class {
                font-weight: bold;
                font-size: 20px;
                color: rgba(37, 42, 51, 255);
            }

            .icon {
                font-size: 50px;
            }

            #vegetarian-icon {
                color: rgba(98, 165, 54, 255);
            }

            #gluten-free-icon {
                color: rgba(255, 194, 12, 255);
            }

            #daity-free-icon {
                color: rgba(68, 162, 234, 255);
            }

            #keto-friendly-icon {
                color: rgba(161, 87, 28, 255);
            }
        }
    }
}
</style>