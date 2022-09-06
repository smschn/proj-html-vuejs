<template>
    <footer>
        <MyFooterSection1 />
        <section id="f2"></section>
    </footer>
</template>

<script>
import MyFooterSection1 from './MyFooterSection1.vue';

export default {
    name: 'MyFooter',
    components: {
        MyFooterSection1
    }
}
</script>

<style scoped lang="scss">
@import '../style/vars.scss';
@import '~@fortawesome/fontawesome-free/css/all.css';


</style>