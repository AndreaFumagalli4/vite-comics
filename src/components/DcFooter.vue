<script>
export default {
    data () {
        return {
            dcComicsItems : [
                {
                    text: 'Characters',
                },
                {
                    text: 'Comics',
                },
                {
                    text: 'Movies',
                },
                {
                    text: 'Tv',
                },
                {
                    text: 'Games',
                },
                {
                    text: 'Videos',
                },
                {
                    text: 'News',
                },
            ],

            shopItems : [
                {
                    text: 'Shop DC',
                },
                {
                    text: 'Shop DC Collectibles',
                },
            ],

            dcItems : [
                {
                    text: 'Terms Of Use',
                },
                {
                    text: 'Privacy policy (new)',
                },
                {
                    text: 'Ad Choices',
                },
                {
                    text: 'Advertising',
                },
                {
                    text: 'Jobs',
                },
                {
                    text: 'Subscriptions',
                },
                {
                    text: 'Talent Workshops',
                },
                {
                    text: 'CPSC Certificates',
                },
                {
                    text: 'Ratings',
                },
                {
                    text: 'Shop Help',
                },
                {
                    text: 'Contact Us',
                },
            ],

            siteItems : [
                {
                    text: 'DC',
                },
                {
                    text: 'MAD Magazine',
                },
                {
                    text: 'DC Kids',
                },
                {
                    text: 'DC Universe',
                },
                {
                    text: 'DC Power Visa',
                },
            ]

        }
    }
}
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
                        <li v-for="dcComicsItem in dcComicsItems">
                            {{ dcComicsItem.text }}
                        </li>
                    </ul>

                    <h4>
                        Shop
                    </h4>
                    <ul>
                        <li v-for="shopItem in shopItems">
                            {{ shopItem.text }}
                        </li>
                    </ul>
                </nav>
                <nav class="dc">
                    <h4>
                        DC
                    </h4>
                    <ul>
                        <li v-for="dcItem in dcItems">
                            {{ dcItem.text }}
                        </li>
                    </ul>
                </nav>
                <nav class="sites">
                    <h4>
                        Sites
                    </h4>
                    <ul>
                        <li v-for="siteItem in siteItems">
                            {{ siteItem.text }}
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
                        <img src="../assets/img/footer-twitter.png" alt="Twitter logo">
                    </li>
                    <li>
                        <img src="../assets/img/footer-youtube.png" alt="Youtube logo">
                    </li>
                    <li>
                        <img src="../assets/img/footer-pinterest.png" alt="Pinterest logo">
                    </li>
                    <li>
                        <img src="../assets/img/footer-periscope.png" alt="Periscope logo">
                    </li>
                </ul>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

    section.footer-top {
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
