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
      <div id="consulting">
        <h5>FUSIONS & AQUISITIONS</h5>
        <h1>Insurance</h1>
        <h1>Consulting</h1>
        <div class="input_first_row">
          <input type="text" placeholder="Name" />
          <input type="email" placeholder="Email" />
        </div>
        <div>
          <input type="number" placeholder="Phone" />
          <select name="info" id="info">
            <option value="">More info</option>
            <option value="Option1">Option1</option>
            <option value="Option2">Option2</option>
            <option value="Option3">Option3</option>
          </select>
        </div>
        <button class="btn btn_green">GET IN TOUCH</button>
        <button class="btn btn_white">READ MORE</button>
      </div>
    </div>
</template>

<script>
export default {
    name: 'MyJumbotron',
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

    #consulting {
      position: absolute;
      right: 15%;
      bottom: 30%;

      h5 {
        color: $c5;
      }

      h1 {
        font-size: 4rem;
        font-weight: bold;
      }

      input,
      select {
        margin-right: 10px;
        margin-bottom: 10px;
        padding: 10px;
        background-color: $c6;
        border: 1px solid $c6;
        border-radius: 4px;
      }

      .input_first_row {
        margin-top: 20px;
      }

      select {
        color: grey;
        width: 47%;
      }

      .btn_white{
        margin-left: 15px;
        background-color: #e1e5e6;
        color: $c2;
      }
    }
  }
</style>