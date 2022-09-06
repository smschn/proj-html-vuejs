<template>
    <section id="section6">
      <div class="container s6 d_flex">
        <div class="s6_left">
          <h5>newsletter</h5>
          <h1><span>Know</span> First</h1>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt consequuntur delectus, iure veniam explicabo quae?</p>
        </div>
        <div class="s6_right">
          <input type="text" placeholder="Name" />
          <input type="email" placeholder="Email" />
          <button class="btn btn_green">subscribe</button>
        </div>
      </div>
    </section>
</template>

<script>
export default {
    name: 'MySection6'
}
</script>

<style scoped lang="scss">
@import '../style/vars.scss';
@import '~@fortawesome/fontawesome-free/css/all.css';

#section6 {
  background-image: url('../assets/img/bg-1.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  height: 380px;
  color: #fff;
  padding: 100px 0;

  .container.s6 {
    justify-content: space-between;

    .s6_left {
      flex-basis: calc(100% / 2 - 20px);
      padding-left: 140px;

      h5 {
        text-transform: uppercase;
        color: $c5;
      }

      h1 {
        font-size: 3rem;
        margin: 25px 0;

        span {
          background-color: $c12;
          border-radius: 5px;
          padding: 10px;
        }
      }

      p {
        color: $c1;
      }
    }

    .s6_right {
      padding-right: 140px;
      
      input,
      button {
        display: block;
      }

      input {
        width: 300px;
        max-width: 300px;
        margin-right: 10px;
        margin-bottom: 10px;
        padding: 10px;
        background-color: $c6;
        border: 1px solid $c6;
        border-radius: 4px;
        opacity: 0.5;
      }

      button {
        text-transform: uppercase;
      }
    }
  }
}
</style>