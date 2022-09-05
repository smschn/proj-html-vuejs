<template>
  <main>
    <MySection1 />
    <MySection2 />
    <section id="section3">
      to do
    </section>
    <MySection4 />
    <section id="section5"></section>
    <section id="section6"></section>
  </main>
</template>

<script>
import MySection1 from './MySection1.vue';
import MySection2 from './MySection2.vue';
import MySection4 from './MySection4.vue';


export default {
    name: 'MyMain',
    components: {
      MySection1,
      MySection2,
      MySection4
    }
}
</script>

<style scoped lang="scss">
@import '../style/vars.scss';
@import '~@fortawesome/fontawesome-free/css/all.css';

#section3 {
  padding: 300px;
}
</style>