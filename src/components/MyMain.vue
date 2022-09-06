<template>
  <main>
    <MySection1 />
    <MySection2 />
    <section id="section3">
      <div class="container s3_first">
        <h5>how it works in practice</h5>
        <h1><span>Process</span> Management</h1>
        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Natus, reprehenderit quasi. Facilis, suscipit dolor voluptatum minima ea fugit exercitationem nam!</p>
      </div>
      <div class="s3_second">
        <div class="circle_card_container">
          <div class="circle">1</div>
          <h3>titolo</h3>
          <p>Lorem ipsum dolor sit amet.</p>
        </div>
        <div class="circle_card_container">
          <div class="circle"></div>
          <h3>titolo</h3>
          <p>Lorem ipsum dolor sit amet.</p>
        </div>
        <div class="circle_card_container">
          <div class="circle"></div>
          <h3>titolo</h3>
          <p>Lorem ipsum dolor sit amet.</p>
        </div>
        <div class="circle_card_container">
          <div class="circle"></div>
          <h3>titolo</h3>
          <p>Lorem ipsum dolor sit amet.</p>
        </div>
        <div class="circle_card_container">
          <div class="circle"></div>
          <h3>titolo</h3>
          <p>Lorem ipsum dolor sit amet.</p>
        </div>
      </div>
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
  padding: 100px;

  .container.s3_first {
    text-align: center;

    h5 {
      text-transform: uppercase;
      color: $c5;
    }

    h1 {
      margin: 20px 0;
      font-size: 3rem;

      span {
      background-color: $c4;
      color: $c2;
      border-radius: 5px;
      padding: 10px;
      }
    }

    p {
      color: grey;
    }
  }

  .s3_second {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    margin-top: 50px;

    .circle_card_container {
      flex-basis: calc(100% / 5);
      text-align: center;
      border-top: 4px solid lightgreen;
      position: relative;

      .circle {
        width: 40px;
        height: 40px;
        border-radius: 50%;
        background-color: lightcoral;
        position: absolute;
        left: 50%;
        transform: translateX(-50%);
        top: -22px;
        text-align: center;
        line-height: 40px;
      }

      h3 {
        margin-top: 30px;
      }
    }


  }
}
</style>