<template>
    <section id="section1">
      <div class="container d_flex">
        <div class="s1_left">
          <h5>ABOUT THE NETWORK</h5>
          <h1>The Company</h1>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Iste deleniti repellat, ex repellendus inventore dolore quia necessitatibus veritatis sequi placeat eum rerum corporis voluptate officia!</p>
          <br>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Inventore, quis.</p>
        </div>
        <div class="s1_right d_flex">
          <div class="square" v-for="(squareContent, index) in squaresContent" v-bind:key="index">
            <i v-bind:class="squareContent.iconClass"></i>
            <h2>{{squareContent.title}}</h2>
            <p>{{squareContent.text}}</p>
          </div>
        </div>
      </div>
    </section>
</template>

<script>
export default {
    name: 'MySection1',
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
        margin: 20px;
        font-size: 3rem;
      }

      p {
        color: grey;
      }
    }

    .s1_right {
      max-width: 50%;
      margin-left: 15px;
      flex-wrap: wrap;

      .square {
        flex-basis: calc(100% / 2 - 10px);
        margin: 5px;

        i {
          margin-right: 10px;
          color: $c2;
          font-size: 1.1rem;
        }

        h2 {
          display: inline-block;
        }

        p {
          margin: 10px 0;
          color: grey;
        }
      }
    }
  }
}
</style>