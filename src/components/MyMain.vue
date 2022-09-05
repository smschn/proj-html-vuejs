<template>
  <main>
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
          <div class="square">quadrato1</div>
          <div class="square">quadrato1</div>
          <div class="square">quadrato1</div>
          <div class="square">quadrato1</div>
        </div>
      </div>
    </section>
    <section id="section2"></section>
    <section id="section3"></section>
    <section id="section4"></section>
    <section id="section5"></section>
    <section id="section6"></section>
  </main>
</template>

<script>
export default {
    name: 'MyMain'
}
</script>

<style scoped lang="scss">
@import '../style/vars.scss';
@import '~@fortawesome/fontawesome-free/css/all.css';

#section1 {
  background-color: $c8;
  padding: 100px;
  color: #fff; //eliminare

  .container {
    justify-content: center;
    padding: 20px;

    .s1_left {
      max-width: 50%;

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
      flex-wrap: wrap;

      .square {
        flex-basis: calc(100% / 2);
      }
    }
  }
}

#section2 {
  background-color: $c4;
  height: 100px;
}
</style>