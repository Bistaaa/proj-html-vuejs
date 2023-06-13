<script>
export default {
    name: "PageFooter"
}
</script>

<template>
    <div id="footer-container">
        <!-- Upper Footer -->
        <section id="upper-footer">
            <!-- order column -->
            <ul id="order-column">
                <h4>ORDER ONLINE</h4>
                <li><a href="#">Appetizers</a></li>
                <li><a href="#">Burgers</a></li>
                <li><a href="#">Pizza</a></li>
                <li><a href="#">Fries</a></li>
                <li><a href="#">Sides</a></li>
                <li><a href="#">Desserts</a></li>
                <li><a href="#">Beverages</a></li>
                <li><a href="#">Specials</a></li>
            </ul>

            <!-- navigate column -->
            <ul id="navigate-column">
                <h4>NAVIGATE</h4>
                <li><a class="yellow" href="#">Home</a></li>
                <li><a href="#">Alternative Home</a></li>
                <li><a href="#">Menu</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">News</a></li>
                <li><a href="#">Contact Us</a></li>
                <li><a href="#">Cart</a></li>
            </ul>

            <!-- information column -->
            <ul id="information-column">
                <h4>INFORMATION</h4>
                <li><a href="#">My Account</a></li>
                <li><a href="#">Terms Of Service</a></li>
                <li><a href="#">Privacy Policy</a></li>
                <img class="badge" src="../assets/img/app-store-badge.png" alt="app-store-badge">
                <img class="badge" src="../assets/img/play-store-badge.png" alt="play-store-badge">
            </ul>

            <!-- opening column -->
            <ul id="opening-column">
                <h4>OPENING HOURS</h4>
                <li>Mon - <span class="yellow">10AM to 11PM</span></li>
                <li>Tue - <span class="yellow">10AM to 11PM</span></li>
                <li>Wed - <span class="yellow">10AM to 11PM</span></li>
                <li>Thur - <span class="yellow">10AM to 11PM</span></li>
                <li>Fri - <span class="yellow">10AM to 11PM</span></li>
                <li>Sat - <span class="yellow">10AM to 1AM</span></li>
                <li>Sun - <span class="yellow">11AM to 10PM</span></li>
            </ul>

            <!-- voucher column -->
            <ul id="voucher-column">
                <h4>VOUCHER</h4>
                <img id="footer-coupon" src="../assets/img/footer-coupon.png" alt="footer-coupon">
                <p>Just Use The Code</p>
                <p class="yellow" id="coupon-code">FIRSTORDER</p>
                <p>At Checkout</p>
            </ul>
        </section>

        <!-- Bottom Footer -->
        <section id="bottom-footer">

        </section>
    </div>
</template>

<style lang="scss">
@use "../styles/partials/mixins.scss" as *;

#footer-container {
    background-image: url(../assets/img/footer-background-scaled.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    width: 100%;
    padding: 150px 12% 250px;

    /* Upper Footer */

    #upper-footer {
        @include my-flex-row;
        justify-content: space-between;

        ul {
            list-style: none;
            color: white;
            @include my-flex-column;
            gap: 20px;
            font-size: 13px;
            font-weight: bold;

            h4 {
                margin-bottom: 20px;
                font-size: 15px;

            }

            a {
                text-decoration: none;
                color: white;
            }

            a:hover {
                color: rgba(252, 220, 49, 255);
            }

            a.yellow {
                color: rgba(252, 220, 49, 255);
            }

            a.yellow:hover {
                color: white;
            }

            .badge {
                width: 150px;
                border: 2px solid white;
                border-radius: 8px;
                margin-bottom: -10px;
            }
        }

        #opening-column {
            gap: 12px;
        }

        #voucher-column {
            @include my-flex-column;
            align-items: center;

            #footer-coupon {
                width: 150px;
            }

            p {
                font-size: 18px;
                margin-bottom: -20px;
            }

            #coupon-code {
                font-size: 22px;
            }
        }
    }

    /* Bottom Footer */
}
</style>