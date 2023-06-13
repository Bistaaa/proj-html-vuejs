<script>
export default {
  name: "PageHeader"
}
</script>

<template>
  <div id="header-container">
    <i class="plus-icons fa-solid fa-plus"></i>

    <!-- Logo + Nav container -->
    <div id="logo-nav-container">
      <img id="logo" src="../assets/img/takeout-logo.png" alt="logo">

      <!-- Nav -->
      <div id="nav-container">
        <ul>
          <li><a href="#">Home <i class="fa-solid fa-angle-down"></i> </a></li>
          <li><a href="#">Order Online</a></li>
          <li><a href="#">About</a></li>
          <li><a href="#">News</a></li>
          <li><a href="#">Contact Us</a></li>
          <li><a href="#"> <i class="fa-solid fa-cart-shopping"></i> </a></li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
@use "../styles/partials/mixins.scss" as *;

#header-container {
  background-image: url(../assets/img/home-background-hero-scaled.jpg);
  background-size: contain;
  background-repeat: no-repeat;
  width: 100%;
  padding: 5px 20%;

  .plus-icons {
    color: white;
    font-size: 10px;
    padding: 15px;
    border-radius: 50%;
    background-color: red;
    position: absolute;
    right: 10px;
    top: 5px;
  }

  #logo-nav-container {
    padding-top: 50px;
    @include my-flex-row;
    justify-content: space-between;
    align-items: center;

    #logo {
      height: 50px;
    }

    #nav-container ul {
      @include my-flex-row;
      gap: 45px;
      font-weight: bold;
      font-size: 20px;
    }

    #nav-container a {
      color: rgb(0, 0, 0);
      text-decoration: none;

    }
  }
}
</style>
