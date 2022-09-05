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
          <div class="square">
            <i class="fa-solid fa-medal"></i>
            <h2>Tradition</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Doloribus, necessitatibus.</p>
          </div>
          <div class="square">
            <i class="fa-solid fa-lock"></i>
            <h2>Security</h2>
            <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Necessitatibus, animi?</p>
          </div>
          <div class="square">
            <i class="fa-regular fa-note-sticky"></i>
            <h2>Certificate</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolores, voluptatibus!</p>
          </div>
          <div class="square">
            <i class="fa-solid fa-graduation-cap"></i>
            <h2>Expertise</h2>
            <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Aperiam, alias?</p>
          </div>
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
    justify-content: space-between;
    padding: 20px;

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

#section2 {
  background-color: $c4;
  height: 100px;
}
</style>