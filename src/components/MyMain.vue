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
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusamus repellat eius quaerat voluptatem est dolorem!</p>
          <button class="btn btn_green">SEE ALL</button>
        </div>
      </div>
      <div class="container s5_bottom d_flex">
        <div class="news_card d_flex">
          <img src="../assets/img/news-1.jpg" alt="aaa">
          <p>Increasing creativity is possibile for everyone</p>
        </div>
        <div class="news_card d_flex">
          <img src="../assets/img/news-2.jpg" alt="aaa">
          <p>Increasing creativity is possibile for everyone</p>
        </div>
        <div class="news_card d_flex">
          <img src="../assets/img/news-3.jpg" alt="aaa">
          <p>Increasing creativity is possibile for everyone</p>
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
    },
    data() {
      return {
        newsData: [
          {
            imgSrc: require('../assets/img/news-1.jpg'),
            text: 'Increasing creativity is possibile for everyone'
          },
          {
            imgSrc: require('../assets/img/news-2.jpg'),
            text: 'Because market research is part of the business plan'
          },
          {
            imgSrc: require('../assets/img/news-3.jpg'),
            text: 'Working from home is now a trend'
          }
        ]
      }
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

  .floated {

    p {
      float: left;
      max-width: 70%;
      color: grey;
    }

    button {
      float: right;
    }
  }

  .floated:after {
    content: "";
    display: table;
    clear: both;
  }

  .s5_bottom {
    justify-content: space-around;
    color: #fff;
    font-weight: bold;

    .news_card {
      flex-basis: calc(100% / 3 - 5px);
      max-height: 340px;
      margin-top: 30px;
      border-radius: 10px;
      position: relative;
      justify-content: center;


      img {
        max-width: 100%;
        max-height: 100%;
        filter: brightness(50%);
        border-radius: 10px;
      }

      p {
        position: absolute;
        bottom: 20%;
        text-align: center;
        max-width: 70%;
      }
    }
  }

}
</style>