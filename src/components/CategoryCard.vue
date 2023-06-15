<script>
export default {
    name: "CategoryCard",
    props: {
        info: Object
    }
}
</script>

<template>
    <div class="category-card">
        <img class="category-img" :src="info.src">
        <div class="black-filter"></div>
        <p class="category-name">{{ info.name }}</p>
    </div>
</template>

<style lang="scss">
@use "../styles/partials/mixins.scss" as *;

.category-card {
    width: calc((100% / 4) - 20px);
    position: relative;

    .category-img {
        width: 100%;
    }

    .black-filter {
        background-color: rgba(0, 0, 0, 0.3);
        position: absolute;
        height: calc(100% - 4px);
        width: 100%;
        top: 0;
        left: 0;
    }

    .category-name {
        color: white;
        font-size: 18px;
        font-weight: bold;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }
}
</style>
