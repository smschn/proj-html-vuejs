<template>
  <main>
    <MySection1 />
    <MySection2 />
    <MySection3 />
    <MySection4 />
    <MySection5 />
    <section id="section6">
      <div class="container">
        <div class="s6_left">
          <h5>newsletter</h5>
          <h1><span>Know</span> First</h1>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt consequuntur delectus, iure veniam explicabo quae?</p>
        </div>
        <div class="s6_right">
          <input type="text" placeholder="Name" />
          <input type="email" palceholder="Email" />
          <button>subscribe</button>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
import MySection1 from './MySection1.vue';
import MySection2 from './MySection2.vue';
import MySection3 from './MySection3.vue';
import MySection4 from './MySection4.vue';
import MySection5 from './MySection5.vue';

export default {
    name: 'MyMain',
    components: {
      MySection1,
      MySection2,
      MySection3,
      MySection4,
      MySection5
    }
}
</script>

<style scoped lang="scss">
@import '../style/vars.scss';
@import '~@fortawesome/fontawesome-free/css/all.css';

#section6 {
  background-image: url('../assets/img/bg-1.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  height: 440px;
  color: #fff;
  padding: 100px 0;
}
</style>