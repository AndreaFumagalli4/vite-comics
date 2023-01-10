<script>
export default {
    name: 'DcMainComic',

    props: {
        cover: String,
        title: String,
        cost: String
    }
}
</script>

<template>
    <div class="card">
        <div class="cover-card">
            <img :src="cover" alt="">
        </div>
        <h4>
            {{ title }}
        </h4>
        <!-- <p>
            {{ cost }}
        </p> -->
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

    div.card {
        width: calc((100% / 6) - 1rem);
        margin: 0 .5rem 1rem;

        h4,
        p {
            color: $title-color;
            text-transform: uppercase;
            font-size: .65rem;
            font-weight: 300;
            padding-top: 1rem;
        }
    }

    // div.card p {
    //     color: $dc-color;
    // }

    div.cover-card {
        width: 100%;
        height: 150px;

        img {
            width: 100%;
            height: 100%;
        }
    }
</style>