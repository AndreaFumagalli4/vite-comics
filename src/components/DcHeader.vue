<script>

</script>

<template>
    <div class="header-container">
        <img src="../assets/img/dc-logo.png" alt="DC Main Logo">
        <nav>
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
                    Collectibles
                </li>
                <li>
                    Videos
                </li>
                <li>
                    Fans
                </li>
                <li>
                    News
                </li>
                <li>
                    Shop
                </li>
            </ul>
        </nav>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
    div.header-container{
        height: 100px;
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
            padding: .5rem .9rem;
        }
    }

</style>
