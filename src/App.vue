<script>
import DcHeader from './components/DcHeader.vue';
import DcMain from './components/DcMain.vue';
import DcFooter from './components/DcFooter.vue';

export default {
    components: {
        DcHeader,
        DcMain,
        DcFooter
    }
}
</script>

<template>
    <header>
        <DcHeader/>
    </header>

    <main>
        <DcMain/>
    </main>

    <footer>
        <DcFooter/>
    </footer>
</template>

<style lang="scss">
@use './styles/general.scss' as *;

</style>
