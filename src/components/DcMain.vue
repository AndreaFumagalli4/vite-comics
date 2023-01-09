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

    <section class="blue-separator">

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

</style>
