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
        <nav>
            <div class="main-logo">
                <img src="../assets/img/dc-logo.png" alt="DC Main Logo">
            </div>
            <ul>
                <li v-for="navItem in navItems" :class="(navItem.active) ? 'active' : '' ">
                    {{ navItem.text }}
                </li>
                
            </ul>
        </nav>
        
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
    div.header-container{
        width: $container-width;
        margin: $container-margin;
    }

    nav {
        display: flex;
        justify-content: space-between;
        height: 100px;

        ul {
            display: flex;
            line-height: calc(100px - .325rem);

            li {
                color: $main-color;
                font-weight: bold;
                text-transform: uppercase;
                font-size: $header-font-size;
                margin: 0 .75rem;
            }
        }
    }

    div.main-logo {
        padding: 1rem 0;

        img {
            height: 100%;
        }
    }
    

    .active {
        color: $dc-color;
        border-bottom: 3px solid $dc-color;
    }

</style>
