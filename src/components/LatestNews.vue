<script>
export default {
    name: "LatestNews"
}
</script>

<template>
    <section id="latest-news">
        <h2>Latest News</h2>

        <button id="more-news-button" class="red-button">READ MORE NEWS <i class="fa-solid fa-circle-right"></i></button>

        <div id="news-container">
            <div class="news-column" id="pancake-burger-column">
                <img src="../assets/img/pancake-burger.jpg" class="news-image">
                <h3>NEW: The Pancake Burger</h3>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Delectus veritatis aspernatur quaerat,
                    perspiciatis, neque accusantium voluptatibus doloribus asperiores exercitationem ullam vero voluptas
                    fugit in eveniet, illum sit vitae deleniti distinctio.</p>
            </div>
            <div class="news-column" id="milkshake-menu-column">
                <img src="../assets/img/new-milkshake-menu.jpg" class="news-image">
                <h3>New Milkshake Menu</h3>
                <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Earum unde inventore quos neque ducimus ab enim
                    vel quo, architecto, error fugit ullam consectetur iusto natus porro minus cum laborum necessitatibus.
                </p>
            </div>
        </div>
    </section>
</template>

<style lang="scss">
@use "../styles/partials/mixins.scss" as *;

#latest-news {
    padding: 150px 20% 200px;
    position: relative;

    h2 {
        font-size: 45px;
    }

    #more-news-button {
        position: absolute;
        right: 20%;
        top: 130px;
    }

    #news-container {
        @include my-flex-row;
        gap: 50px;
        margin-top: 50px;

        .news-column {
            width: calc(100% / 2);

            .news-image {
                width: 100%;
            }

            h3 {
                font-size: 40px;
                color: rgba(37, 42, 51, 255);
                text-align: center;
                margin-top: 30px;
            }

            p {
                font-size: 15px;
                color: rgba(37, 42, 51, 255);
                text-align: center;
                margin: 0 8%;
            }
        }

    }
}
</style>