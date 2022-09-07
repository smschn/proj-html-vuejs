<template>
      <div id="jumbotron">
      <div class="header_middle">
        <div class="container navbar d_flex">
          <div class="d_flex logo">
            <span class="logo_left">NEX</span>
            <span class="logo_right">GEN</span>
          </div>
          <ul class="d_flex">
            <li v-for="(link, index) in navbarLinks" v-bind:key="index"><a v-bind:href="link.url">{{link.text}}</a></li>
            <button class="btn btn_green">GET IN TOUCH</button>
          </ul>
        </div>
      </div>
      <MyJumbotronCard />
    </div>
</template>

<script>
import MyJumbotronCard from './MyJumbotronCard.vue';
export default {
    name: 'MyJumbotron',
    components: {
      MyJumbotronCard
    },
    data() {
        return {
            navbarLinks: [
                {
                    text: 'home',
                    url: '#'
                },
                {
                    text: 'about',
                    url: '#'
                },
                {
                    text: 'services',
                    url: '#'
                },
                {
                    text: 'process',
                    url: '#'
                },
                {
                    text: 'team',
                    url: '#'
                },
                {
                    text: 'blog',
                    url: '#'
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import '../style/general.scss';
@import '../style/vars.scss';

#jumbotron {
    background-image: url('../assets/img/bg-6.jpg');
    background-repeat: no-repeat;
    background-image: cover;
    background-position-y: -100px;
    background-position-x: -110px;
    position: relative;
    height: 800px;

    .header_middle {
      padding: 20px 10px 10px 10px;
    
      .navbar {
        justify-content: space-between;
        text-decoration: none;

        .logo {
          font-weight: bold;
          letter-spacing: 5px;

          .logo_left {
            border-top-left-radius: 20px;
            border-bottom-left-radius: 20px;
            background-color: $c4;
            padding: 10px 1px 10px 20px;
            color: $c5;
            margin-right: 2px;
          }
        }

        div,
        ul {
          align-items: center;
        }
      
        li {
          padding: 0 15px;
          list-style: none;
          text-transform: uppercase;

          a {
            text-decoration: none;
            color: $c3;
          }
        }

        .btn_green {
          margin-left: 10px;
        }
      }
    }
}
</style>