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

    <div id="demos-container" class="right-square-container">
      <i class="fa-solid fa-folder"></i>
      <p>Demos</p>
    </div>

    <div id="on-sale-container" class="right-square-container">
      <p id="right-square-price"><sup>$</sup>39</p>
      <p>On Sale</p>
    </div>

    <div id="title-container">
      <p class="white">Hungry?</p>
      <h1 class="yellow">Great Food</h1>
      <h1 class="white">Delivered</h1>
      <a href="#" id="view-menu" class="white"> VIEW OUR MENU <i class="fa-solid fa-circle-right"></i></a>
    </div>

    <div id="takeout-pros">
      <span class="pros"><i class="fa-regular fa-clock"></i> 24/7 DELIVERY</span>
      <span class="pros"><i class="fa-solid fa-burger"></i> OVER 100 DISHES</span>
      <span class="pros"><i class="fa-solid fa-mobile-screen-button"></i> IN APP ORDERING</span>
      <span class="pros"><i class="fa-solid fa-car"></i> FAST DELIVERY</span>
    </div>
  </div>
</template>

<style lang="scss">
@use "../styles/partials/mixins.scss" as *;

#header-container {
  background-image: url(../assets/img/home-background-hero-scaled.jpg);
  background-size: cover;
  background-repeat: no-repeat;
  width: 100%;
  position: relative;

  .plus-icons {
    color: white;
    font-size: 14px;
    padding: 18px;
    border-radius: 50%;
    background-color: red;
    position: absolute;
    top: 50px;
    right: 10px;
  }

  #logo-nav-container {
    padding-top: 50px;
    @include my-flex-row;
    justify-content: space-between;
    align-items: center;
    padding: 125px 20% 0;

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
      color: white;
      text-decoration: none;

    }

    #nav-container a:hover {
      color: rgba(252, 220, 49, 255);
    }
  }

  .right-square-container {
    height: 65px;
    width: 65px;
    border-radius: 10px;
    background-color: white;
    color: rgba(51, 71, 91, 255);
    padding: 10px;
    @include my-flex-column;
    align-items: center;
    font-size: 12px;
    font-weight: bold;

    #right-square-price {
      color: rgba(103, 189, 125, 255);
      font-size: 30px;
      font-weight: 600;

      sup {
        vertical-align: super;
        font-size: 17px;
        font-weight: bold;
      }
    }
  }

  #demos-container {
    position: absolute;
    top: 200px;
    right: 10px;

    i {
      font-size: 25px;
    }
  }

  #on-sale-container {
    position: absolute;
    top: 270px;
    right: 10px;
  }

  #title-container {
    padding: 250px 20% 400px;

    p:first-of-type {
      font-size: 40px;
      font-weight: 600;
    }

    h1 {
      font-size: 80px;
    }

    h1.white {
      margin-bottom: 50px;
    }

    #view-menu {
      background-color: rgba(206, 26, 38, 255);
      padding: 11px 25px;
      border-radius: 20px;
      text-decoration: none;
      font-weight: 600;
      font-size: 14px;
    }
  }

  #takeout-pros {
    @include my-flex-row;
    justify-content: space-between;
    padding: 30px;
    margin-left: 20%;
    width: 60%;
    background-color: white;
    position: absolute;
    bottom: -40px;

    .pros {
      font-weight: 600;
    }

    i {
      margin-right: 10px;
    }
  }
}
</style>
