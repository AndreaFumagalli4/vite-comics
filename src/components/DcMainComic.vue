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
            {{ title }} -- 
        </h4>
        <span>{{ cost }}</span> 
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

    div.card {
        width: calc((100% / 6) - 1.5rem);
        margin: 0 .75rem 1rem;

        h4,
        span {
            color: $title-color;
            text-transform: uppercase;
            font-size: .65rem;
            font-weight: 300;
            padding-top: 1rem;
        }

        span {
            color: $dc-color;
        }
    }

    div.cover-card {
        width: 100%;
        height: 150px;

        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: top;
        }
    }
</style>