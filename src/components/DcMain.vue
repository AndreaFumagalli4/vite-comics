<script>
import DcMainComic from './DcMainComic.vue';

export default {
    components: {
        DcMainComic,
    },

    data () {
        return {
            listItems: [
                {
                    text: 'Digital Comics',
                    imageName: 'buy-comics-digital-comics.png',
                },
                {
                    text: 'DC Merchandise',
                    imageName: 'buy-comics-merchandise.png',
                },
                {
                    text: 'Subscription',
                    imageName: 'buy-comics-subscriptions.png',
                },
                {
                    text: 'Comic Shop Locator',
                    imageName: 'buy-comics-shop-locator.png',
                },
                {
                    text: 'DC Power Visa',
                    imageName: 'buy-dc-power-visa.svg',
                },
            ],

            comicItems : [
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel"
                }
            ],
        }
    },

    methods: {
        getImagePath: function(imgPath) {
            return new URL(`../assets/img/${imgPath}`, import.meta.url).href;
        }
    }
}
</script>

<template>
    <section class="comic">
        <div class="main-container">
            <div class="title">
                <h3>
                    Current series
                </h3>
            </div>
            <div class="comics">
                <DcMainComic v-for="comicItem in comicItems"
                :cover="comicItem.thumb"
                :title="comicItem.series"
                :cost="comicItem.price" />
            </div>
            <div class="button">
                <button>
                    Load More
                </button>
            </div>
        </div>
    </section>

    <section class="blue-separator">
        <div class="banner">
            <div class="banner-element" v-for="listItem in listItems">
                <img :src="getImagePath(listItem.imageName)" alt="`${listItem.text}`">
                <p>
                    {{ listItem.text }}
                </p>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

    section.comic {
        background-color: $bg-color;
    }

    div.main-container {
        width: $container-width;
        margin: $container-margin;
        position: relative;

        div.title {
            position: absolute;
            top: -20px;
            left: 0;

            h3 {
                color: $title-color;
                padding: .7rem 1rem;
                background-color: $dc-color;
                text-transform: uppercase;
            }
        }
    }

    div.comics {
        display: flex;
        flex-wrap: wrap;
        padding-top: 3rem;
    }

    div.button {
        text-align: center;
        padding: 1.5rem 0 1rem;

        button {
            border: none;
            background-color: $dc-color;
            color: $title-color;
            text-transform: uppercase;
            font-weight: 700;
            font-size: .6rem;
            padding: .5rem 2.5rem;
        }
    }

    section.blue-separator {
        background-color: $dc-color;
        height: 100px;
    }

    div.banner{
        height: 100%;
        width: $container-width;
        margin: $container-margin;
        display: flex;
        justify-content: space-around;

        div.banner-element {
            display: flex;
            align-items: center;

            img {
                height: 40px;
                margin-right: 1rem;
            }

            p {
                font-size: .75rem;
                text-transform: uppercase;
                color: $title-color;
            }
        }
    }

</style>
