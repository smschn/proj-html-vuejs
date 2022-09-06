<template>
  <main>
    <MySection1 />
    <MySection2 />
    <MySection3 />
    <MySection4 />
    <section id="section5">
      <div class="container">
        <h5>our editorial content</h5>
        <h1>Latest <span>News</span></h1>
        <div class="floated">
          <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Illum vitae rerum magni? Provident magni nostrum dolore doloribus vel. Tempora provident veritatis dolore tenetur dicta ratione ea minima eveniet rem qui.</p>
          <button class="btn btn_green">SEE ALL</button>
        </div>
      </div>
    </section>
    <section id="section6"></section>
  </main>
</template>

<script>
import MySection1 from './MySection1.vue';
import MySection2 from './MySection2.vue';
import MySection3 from './MySection3.vue';
import MySection4 from './MySection4.vue';

export default {
    name: 'MyMain',
    components: {
      MySection1,
      MySection2,
      MySection3,
      MySection4
    }
}
</script>

<style scoped lang="scss">
@import '../style/vars.scss';
@import '~@fortawesome/fontawesome-free/css/all.css';

#section5 {
  padding: 100px 0;

  h5 {
    text-transform: uppercase;
    color: $c5;
  }

  h1 {
    font-size: 3rem;
    margin: 25px 0;

    span {
      background-color: $c4;
      color: $c2;
      border-radius: 5px;
      padding: 10px;
    }
  }

  .floated:after {
    content: "";
    display: table;
    clear: both;

    p {
      float: left;
    }

    button {
      float: right;
    }
  }
}
</style>