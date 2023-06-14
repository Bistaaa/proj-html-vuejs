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

        <div id="main-image-container">
            <img id="main-wave" src="../assets/img/svg-0.svg" alt="main-wave">
            <img id="wave-2" src="../assets/img/svg-0.svg" alt="wave-2">
            <img id="wave-3" src="../assets/img/svg-0.svg" alt="wave-3">
            <img id="wave-4" src="../assets/img/svg-0.svg" alt="wave-4">
        </div>

    </section>

    <!-- Menu Categories -->
    <section id="menu-categories">
        <h2>Menu Categories</h2>

        <button id="view-menu" class="red-button">VIEW THE FULL MENU <i class="fa-solid fa-circle-right"></i></button>

        <div id="menu-categories-container">

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

    <!-- Ordering App -->
    <section id="ordering-app">
        <p>Download Our</p>
        <h2 class="yellow">Ordering App</h2>
        <div id="store-container">
            <img class="download-badge" src="../assets/img/app-store-badge.png">
            <img class="download-badge" src="../assets/img/play-store-badge.png">
        </div>
    </section>

    <!-- Latest News -->
    <section id="latest-news">
        <h2>Menu Categories</h2>

        <button id="view-menu" class="red-button">READ MORE NEWS <i class="fa-solid fa-circle-right"></i></button>
    </section>
</template>

<style lang="scss">
@use "../styles/partials/mixins.scss" as *;

/* Popular Dishes */
#popular-dishes {
    margin-top: 100px;

    h2 {
        text-align: center;
        font-size: 40px;
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


/* Menu Categories */
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

/* Ordering App */
#ordering-app {
    padding: 200px 20% 0;
    width: 100%;
    height: 600px;
    background-image: url(../assets/img/app-ordering-scaled.jpg);
    background-size: cover;
    background-position: center;

    p {
        font-size: 40px;
        font-weight: bold;
        color: white;
        margin-bottom: -15px;
    }

    h2 {
        font-size: 80px;
    }

    #store-container {
        @include my-flex-row;
        gap: 20px;

        .download-badge {
            height: 50px;
            margin-top: 50px;
        }
    }
}

/* Latest News */
#latest-news {
    padding: 150px 20% 200px;
}
</style>