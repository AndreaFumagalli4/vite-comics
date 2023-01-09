<script>
export default {
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
            ]
        }
    },

    methods: {
        getImagePath: function(imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    }
}

</script>

<template>
    <section>
        <div class="main-container">
            <h3>
                Content goes here
            </h3>
        </div>
    </section>

    <section class="blue-separator">
        <div class="container">
            <ul>
                <li v-for="listItem in listItems">
                    <div>
                        <img :src="getImagePath(`../assets/img/${listItem.imageName}`)" alt="`${listItem.imageName}`">
                    </div>
                    <p>
                        {{ listItem.text }}
                    </p>
                </li>
            </ul>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

    section {
        height: 15vh;
        background-color: black;
    }

    div.main-container {
        height: 100%;
        width: $container-width;
        margin: $container-margin;
        display: flex;
        align-items: center;

        h3{
            color: $title-color;
            font-size: 1.25rem;
        }
    }

    section.blue-separator {
        background-color: $dc-color;
        height: 15vh;
    }

    div.container{
        width: $container-width;
        margin: $container-margin;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;

        ul {
            display: flex;
            justify-content: space-between;
            align-items: center;

            li {
                padding: 0 1rem;
                font-size: .7rem;
                font-weight: 300;
                text-transform: uppercase;
                color: $title-color;
                display: flex;
                align-items: center;
            }
        }
    }

    li div {
        width: 55px;
        height: 55px;
        margin-right: .5rem;

        img {
            height: 80%;
            width: 80%;
            position: relative;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }
    }

</style>
