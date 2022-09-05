<template>
  <header>
    <div class="header_top">
      <div class="container">
        <ul>
          <li><i class="fa-solid fa-clock"></i></li>
          <li>Open Hours: Mon - Sat - 9:00 - 18:00</li>        
        </ul>
        <ul>
          <li><i class="fa-solid fa-phone"></i> +1 (305) 1234-5678</li> <!-- non posso metterli nel ciclo perché va in conflitto il font -->
          <li><i class="fa-solid fa-envelope"></i> hello@example.com</li>
          <li v-for="(link, index) in headerTopLinks" v-bind:key="index">
            <i v-bind:class="link.iconClass">{{link.text}}</i>
          </li>
        </ul>
      </div>
    </div>
    <MyJumbotron />
  </header>
</template>

<script>
import MyJumbotron from './MyJumbotron.vue';

export default {
    name: 'MyHeader',
    components: {
      MyJumbotron
    },
    data() {
      return {
        headerTopLinks: [
          {
            iconClass: 'fa-brands fa-facebook-f',
            text: ''
          },
          {
            iconClass: 'fa-brands fa-twitter',
            text: ''
          },
          {
            iconClass: 'fa-brands fa-linkedin-in',
            text: ''
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
}
</style>