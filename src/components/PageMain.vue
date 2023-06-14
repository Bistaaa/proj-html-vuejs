<script>
import PopularDishes from './PopularDishes.vue'
import MenuCategories from './MenuCategories.vue'
import OrderingApp from './OrderingApp.vue'
import LatestNews from './LatestNews.vue'

export default {
    name: "PageMain",
    components: {
        PopularDishes,
        MenuCategories,
        OrderingApp,
        LatestNews
    }
}
</script>

<template>
    <PopularDishes />
    <MenuCategories />
    <OrderingApp />
    <LatestNews />
</template>

<style lang="scss"></style>