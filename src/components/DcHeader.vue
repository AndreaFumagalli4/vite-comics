<script>
export default {
    data () {
        return {
            navItems : [
                {
                    text: 'Characters',
                    active: false,
                },
                {
                    text: 'Comics',
                    active: true,
                },
                {
                    text: 'Movies',
                    active: false,
                },
                {
                    text: 'Tv',
                    active: false,
                },
                {
                    text: 'Games',
                    active: false,
                },
                {
                    text: 'Collectibles',
                    active: false,
                },
                {
                    text: 'Videos',
                    active: false,
                },
                {
                    text: 'Fans',
                    active: false,
                },
                {
                    text: 'News',
                    active: false,
                },
                {
                    text: 'Shop',
                    active: false,
                },
            ]
        }
    }
}

</script>

<template>
    <div class="header-container">
        <img src="../assets/img/dc-logo.png" alt="DC Main Logo">
        <nav>
            <ul>
                <li v-for="navItem in navItems"
                :class="(navItem.active) ? 'active' : '' ">
                    {{ navItem.text }}
                </li>
                
            </ul>
        </nav>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
    div.header-container{
        height: 15vh;
        width: $container-width;
        margin: $container-margin;
        display: flex;
        justify-content: space-between;
        align-items: center;

        img {
            width: 60px;
        }
    }

    nav ul {
        display: flex;

        li {
            color: $main-color;
            font-weight: bold;
            text-transform: uppercase;
            font-size: $header-font-size;
            padding: 2.65rem .9rem;
        }
    }

    .active {
        color: $dc-color;
        border-bottom: 2px solid $dc-color;
    }

</style>
