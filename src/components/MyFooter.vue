<template>
    <footer>
        <MyFooterSection1 />
        <MyFooterSection2 />
    </footer>
</template>

<script>
import MyFooterSection1 from './MyFooterSection1.vue';
import MyFooterSection2 from './MyFooterSection2.vue';

export default {
    name: 'MyFooter',
    components: {
        MyFooterSection1,
        MyFooterSection2
    }
}
</script>

<style scoped lang="scss">
@import '../style/vars.scss';
@import '~@fortawesome/fontawesome-free/css/all.css';
</style>