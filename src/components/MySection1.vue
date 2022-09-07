<template>
    <section id="section1">
      <div class="container d_flex">
        <div class="s1_left">
          <h5>ABOUT THE NETWORK</h5>
          <h1><span>The</span> Company</h1>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Iste deleniti repellat, ex repellendus inventore dolore quia necessitatibus veritatis sequi placeat eum rerum corporis voluptate officia!</p>
          <br>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Inventore, quis.</p>
        </div>
        <div class="s1_right d_flex">
          <MySection1Card v-for="(square, index) in squaresContent" v-bind:key="index" :squareProps="square" />
        </div>
      </div>
    </section>
</template>

<script>
import MySection1Card from './MyScetion1Card.vue';

export default {
    name: 'MySection1',
    components: {
      MySection1Card
    },
    data() {
        return {
            squaresContent: [
                {
                    iconClass: 'fa-solid fa-award',
                    title: 'Tradition',
                    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Doloribus, necessitatibus.'
                },
                {
                    iconClass: 'fa-solid fa-lock',
                    title: 'Security',
                    text: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Necessitatibus, animi?'
                },
                {
                    iconClass: 'fa-regular fa-pen-to-square',
                    title: 'Certificate',
                    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolores, voluptatibus!'
                },
                {
                    iconClass: 'fa-solid fa-graduation-cap',
                    title: 'Expertise',
                    text: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Aperiam, alias?'
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import '../style/vars.scss';
@import '~@fortawesome/fontawesome-free/css/all.css';

#section1 {
  background-color: $c8;
  padding: 100px 0;
  color: #fff;

  .container {
    justify-content: space-between;
    padding: 20px;
    width: 100%;

    .s1_left {
      max-width: 50%;
      margin-right: 15px;

      h5 {
        color: $c5;
      }

      h1 {
        margin: 25px 0;
        font-size: 3rem;

        span {
          background-color: $c12;
          border-radius: 5px;
          padding: 10px;
        }
      }

      p {
        color: grey;
      }
    }

    .s1_right {
      max-width: 50%;
      margin-left: 15px;
      flex-wrap: wrap;
    }
  }
}
</style>