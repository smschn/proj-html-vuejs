<template>
    <section id="section2">
      <div class="container">
        <h5>our business areas</h5>
        <h1>Excellence in <span>Services</span></h1>
        <div class="floated">
          <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Illum vitae rerum magni? Provident magni nostrum dolore doloribus vel. Tempora provident veritatis dolore tenetur dicta ratione ea minima eveniet rem qui.</p>
          <button class="btn btn_green">SEE ALL</button>
        </div>
        <div class="services_container d_flex">
          <div class="services_card" v-for="(servicesCard, index) in servicesCardsContent" v-bind:key="index">
            <i v-bind:class="servicesCard.iconClass"></i>
            <h3>{{servicesCard.title}}</h3>
            <p>{{servicesCard.text}}</p>
            <i class="fa-solid fa-arrow-right"></i>
          </div>
        </div>
      </div>
    </section>
</template>

<script>
export default {
    name: 'MySection2',
    data() {
        return {
            servicesCardsContent: [
                {
                    iconClass: 'fa-solid fa-network-wired f_icon',
                    title: 'Audit & Assurance',
                    text: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Doloremque, necessitatibus?'
                },
                {
                    iconClass: 'fa-solid fa-briefcase f_icon',
                    title: 'Financial Advisory',
                    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Cupiditate, exercitationem.'
                },
                {
                    iconClass: 'fa-solid fa-chart-simple f_icon',
                    title: 'Analytics and M&A',
                    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolores, quaerat.'
                },
                {
                    iconClass: 'fa-solid fa-plane f_icon',
                    title: 'Middle Marketing',
                    text: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Aperiam, rem.'
                },
                {
                    iconClass: 'fa-solid fa-scale-balanced f_icon',
                    title: 'Legal Consulting',
                    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Enim, ea!'
                },
                {
                    iconClass: 'fa-solid fa-gavel f_icon',
                    title: 'Regulatory Risk',
                    text: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Voluptate, non?'
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import '../style/vars.scss';
@import '~@fortawesome/fontawesome-free/css/all.css';

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