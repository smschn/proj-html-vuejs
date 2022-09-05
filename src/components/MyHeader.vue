<template>
  <header>
    <div class="header_top">
      <div class="container">
        <ul>
          <li><i class="fa-solid fa-clock"></i></li>
          <li>Open Hours: Mon - Sat - 9:00 - 18:00</li>        
        </ul>
        <ul>
          <li><i class="fa-solid fa-phone"></i> +1 (305) 1234-5678</li>
          <li><i class="fa-solid fa-envelope"></i> hello@example.com</li>
          <li><i class="fa-brands fa-facebook-f"></i></li>
          <li><i class="fa-brands fa-twitter"></i></li>
          <li><i class="fa-brands fa-linkedin-in"></i></li>
        </ul>
      </div>
    </div>
    <div class="header_middle">
      <div class="container navbar d_flex">
        <div class="d_flex logo">
          <span class="logo_left">NEX</span>
          <span class="logo_right">GEN</span>
        </div>
        <ul class="d_flex">
          <li v-for="(link, index) in navbarLinks" v-bind:key="index"><a v-bind:href="link.url">{{link.text}}</a></li>
          <button class="btn">GET IN TOUCH</button>
        </ul>
      </div>
    </div>
    <div id="jumbotron">
      jumbo
    </div>
  </header>
</template>

<script>
export default {
    name: 'MyHeader',
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
          },
        ]
      }
    }
}
</script>

<style lang="scss" scoped>
@import '../style/vars.scss';
@import '~@fortawesome/fontawesome-free/css/all.css';

header {

  .header_top {
    background-color: $c3;
    color: $c1;
    
    .container {
      display: flex;
      justify-content: space-between;
      }
      
    ul {
      display: flex;
      
      li {
        padding: 15px;
        list-style: none;
      }
    }
  }

  .header_middle {
    padding: 10px;
    
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

      .btn {
        background-color: $c2;
        color: #fff;
      }
    }
  }
}
</style>