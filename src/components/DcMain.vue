<script>

</script>

<template>
    <section>
        <div class="main-container">
            <h3>
                Content goes here
            </h3>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

    section {
        height: 100px;
        background-color: black;
    }

    div.main-container {
        height: 100%;
        width: $container-width;
        margin: $container-margin;
        display: flex;
        align-items: center;

        h3{
            color: white;
            font-size: 1.25rem;
        }
    }

</style>
