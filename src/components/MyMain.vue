<template>
  <main>
    <MySection1 />
    <MySection2 />
    <section id="section3"></section>
    <section id="section4"></section>
    <section id="section5"></section>
    <section id="section6"></section>
  </main>
</template>

<script>
import MySection1 from './MySection1.vue';
import MySection2 from './MySection2.vue';


export default {
    name: 'MyMain',
    components: {
      MySection1,
      MySection2
    }
}
</script>

<style scoped lang="scss">
@import '../style/vars.scss';
@import '~@fortawesome/fontawesome-free/css/all.css';


</style>