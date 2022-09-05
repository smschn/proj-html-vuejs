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
            <i class="fa-solid fa-award"></i>
            <h2>Tradition</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Doloribus, necessitatibus.</p>
          </div>
          <div class="square">
            <i class="fa-solid fa-lock"></i>
            <h2>Security</h2>
            <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Necessitatibus, animi?</p>
          </div>
          <div class="square">
            <i class="fa-regular fa-pen-to-square"></i>
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
    <section id="section2">
      <div class="container">
        <h5>our business areas</h5>
        <h1>Excellence in <span>Services</span></h1>
        <div class="floated">
          <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Illum vitae rerum magni? Provident magni nostrum dolore doloribus vel. Tempora provident veritatis dolore tenetur dicta ratione ea minima eveniet rem qui.</p>
          <button class="btn btn_green">SEE ALL</button>
        </div>
        <div class="services_container d_flex">
          <div class="services_card">
            <i class="fa-solid fa-network-wired f_icon"></i>
            <h3>Audit & Assurance</h3>
            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Doloremque, necessitatibus?</p>
            <i class="fa-solid fa-arrow-right"></i>
          </div>
          <div class="services_card">
            <i class="fa-solid fa-network-wired f_icon"></i>
            <h3>Audit & Assurance</h3>
            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Doloremque, necessitatibus?</p>
            <i class="fa-solid fa-arrow-right"></i>
          </div>
          <div class="services_card">
            <i class="fa-solid fa-network-wired f_icon"></i>
            <h3>Audit & Assurance</h3>
            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Doloremque, necessitatibus?</p>
            <i class="fa-solid fa-arrow-right"></i>
          </div>
          <div class="services_card">
            <i class="fa-solid fa-network-wired f_icon"></i>
            <h3>Audit & Assurance</h3>
            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Doloremque, necessitatibus?</p>
            <i class="fa-solid fa-arrow-right"></i>
          </div>
          <div class="services_card">
            <i class="fa-solid fa-network-wired f_icon"></i>
            <h3>Audit & Assurance</h3>
            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Doloremque, necessitatibus?</p>
            <i class="fa-solid fa-arrow-right"></i>
          </div>
          <div class="services_card">
            <i class="fa-solid fa-network-wired f_icon"></i>
            <h3>Audit & Assurance</h3>
            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Doloremque, necessitatibus?</p>
            <i class="fa-solid fa-arrow-right"></i>
          </div>
        </div>
      </div>
    </section>
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

#section2 {
  background-color: $c9;
  padding: 100px 0;

  h5 {
    color: $c5;
    text-transform: uppercase;
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

  p {
    color: grey;
    float: left;
    max-width: 70%;
  }
    
  .btn {
    float: right;
  }

  .floated:after { // clearfix rule
    content: "";
    display: table;
    clear: both;
    
  }

  .services_container {
    margin: 45px 0px;
    flex-wrap: wrap;
    justify-content: space-between;

    .services_card {
      flex-basis: calc(100% / 3 - 20px);
      margin: 20px 0;
      padding: 30px;
      border-radius: 5px;
      position: relative;
      background-color: #fff;

      .f_icon {
        font-size: 2rem;
        color: $c2;
      }

      h3 {
        margin: 20px 0;
      }

      .fa-arrow-right {
        position: absolute;
        right: 10%;
        top: 30px;
        color: $c11;
      }
    }
  }
}
</style>