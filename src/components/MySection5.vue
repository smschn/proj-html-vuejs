<template>
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
        <MySection5Card v-for="(news, index) in newsData" v-bind:key="index" :newsProps="news" />
      </div>
    </section>
</template>

<script>
import MySection5Card from './MySection5Card.vue';

export default {
    name: 'MySection5',
    components: {
      MySection5Card
    },
    data() {
      return {
        newsData: [
          {
            imgSrc: require('../assets/img/news-1.jpg'),
            alt: 'News1',
            text: 'Increasing creativity is possibile for everyone'
          },
          {
            imgSrc: require('../assets/img/news-2.jpg'),
            alt: 'News2',
            text: 'Because market research is part of the business plan'
          },
          {
            imgSrc: require('../assets/img/news-3.jpg'),
            alt: 'News3',
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
    line-height: 37px;

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
  }
}
</style>