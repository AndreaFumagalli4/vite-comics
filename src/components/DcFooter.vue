<script>

</script>

<template>
    <section class="footer-top">
        <div class="container">
            <div class="navs">
                <nav class="dc-nav">
                    <h4>
                        DC Comics
                    </h4>
                    <ul>
                        <li>
                            Characters
                        </li>
                        <li>
                            Comics
                        </li>
                        <li>
                            Movies
                        </li>
                        <li>
                            Tv
                        </li>
                        <li>
                            Games
                        </li>
                        <li>
                            Videos
                        </li>
                        <li>
                            News
                        </li>
                    </ul>

                    <h4>
                        Shop
                    </h4>
                    <ul>
                        <li>
                            Shop DC
                        </li>
                        <li>
                            Shop DC Collectibles
                        </li>
                    </ul>
                </nav>
                <nav class="dc">
                    <h4>
                        DC
                    </h4>
                    <ul>
                        <li>
                            Terms of Use
                        </li>
                        <li>
                            Privacy policy (new)
                        </li>
                        <li>
                            Terms of Use
                        </li>
                        <li>
                            Terms of Use
                        </li>
                        <li>
                            Terms of Use
                        </li>
                        <li>
                            Terms of Use
                        </li>
                        <li>
                            Terms of Use
                        </li>
                        <li>
                            Terms of Use
                        </li>
                        <li>
                            Terms of Use
                        </li>
                        <li>
                            Terms of Use
                        </li>
                        <li>
                            Terms of Use
                        </li>
                    </ul>
                </nav>
                <nav class="sites">
                    <h4>
                        sites
                    </h4>
                    <ul>
                        <li>
                            DC
                        </li>
                        <li>
                            DC
                        </li>
                        <li>
                            DC
                        </li>
                        <li>
                            DC
                        </li>
                        <li>
                            DC
                        </li>
                    </ul>
                </nav>
            </div>
            <div class="image-container"></div>
        </div>
    </section>

    <section class="footer-bottom">
        <div class="container">
            <a href="#">Sign-up now</a>
            <div class="follow">
                <h4>
                    Follow Us
                </h4>
                <ul>
                    <li>
                        <img src="../assets/img/footer-facebook.png" alt="Facebook logo">
                    </li>
                    <li>
                        <img src="../assets/img/footer-facebook.png" alt="Facebook logo">
                    </li>
                    <li>
                        <img src="../assets/img/footer-facebook.png" alt="Facebook logo">
                    </li>
                    <li>
                        <img src="../assets/img/footer-facebook.png" alt="Facebook logo">
                    </li>
                    <li>
                        <img src="../assets/img/footer-facebook.png" alt="Facebook logo">
                    </li>
                </ul>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

    section.footer-top {
        // height: 350px;
        background-image: url('../assets/img/footer-bg.jpg');
        background-position: center;
        background-size: cover;
        background-repeat: no-repeat;
        color: $main-color;
    }

    div.container {
        width: $container-width;
        margin: $container-margin;
        display: flex;
        justify-content: space-between;
    }

    div.navs {
        display: flex;
        padding: 2rem 0;

        nav {
            margin-right: 2rem;
        }
    }

    nav.dc-nav ul {
        padding-bottom: .75rem;
    }

    div.navs nav ul li {
        font-size: .6rem;
        padding: .15rem 0;

    }

    h4 {
        text-transform: uppercase;
        color: $title-color;
        padding-bottom: .75rem;
        font-size: .9rem;
    }
    
    div.image-container {
        width: 50%;
        background-image: url('../assets/img/dc-logo-bg.png');
        background-position: center;
        background-size: cover;
    }

    section.footer-bottom {
        background-color: #303030;
        height: 100px;

        div.container {
            height: 100%;
            align-items: center;

            a {
                padding: 1rem;
                text-transform: uppercase;
                border: 2px solid $dc-color;
            }
        }
    }

    div.follow {
        display: flex;
        align-items: center;

        h4{
            padding: 0 1rem 0 0;
            color: $dc-color;
        }

        ul {
            display: flex;

            li {
                padding-right: .75rem;
            }
        }
    }
</style>
