<template>
  <main>
    <MySection1 />
    <MySection2 />
    <MySection3 />
    <MySection4 />
    <MySection5 />
    <MySection6 />
  </main>
</template>

<script>
import MySection1 from './MySection1.vue';
import MySection2 from './MySection2.vue';
import MySection3 from './MySection3.vue';
import MySection4 from './MySection4.vue';
import MySection5 from './MySection5.vue';
import MySection6 from './MySection6.vue';

export default {
    name: 'MyMain',
    components: {
      MySection1,
      MySection2,
      MySection3,
      MySection4,
      MySection5,
      MySection6
    }
}
</script>

<style scoped lang="scss">
@import '../style/vars.scss';
@import '~@fortawesome/fontawesome-free/css/all.css';
</style>