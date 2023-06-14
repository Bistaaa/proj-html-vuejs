<script>
export default {
    name: "OrderingApp"
}
</script>

<template>
    <section id="ordering-app">
        <p>Download Our</p>
        <h2 class="yellow">Ordering App</h2>
        <div id="store-container">
            <img class="download-badge" src="../assets/img/app-store-badge.png">
            <img class="download-badge" src="../assets/img/play-store-badge.png">
        </div>
    </section>
</template>

<style lang="scss">
@use "../styles/partials/mixins.scss" as *;

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
</style>