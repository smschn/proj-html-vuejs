<template>
    <section id="section4">
      <div class="container d_flex">
        <div class="s4_left">
          <div>
            <h5>we like what we do</h5>
            <h1><span>Team</span> of Experts</h1>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dolores consequatur molestiae fugiat molestias cupiditate repellat ullam quod exercitationem odio unde.</p>
          </div>
          <div class="employee_container d_flex">
            <MySection4Card v-for="(employee, index) in employees" v-bind:key="index" :employeeProps="employee" />
          </div>
        </div>
        <div class="s4_right">
          <div class="s4r_top"></div>
          <div class="s4r_bottom">
            <h4>President Speech</h4>
            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Voluptates ullam eaque eum earum id sint.</p>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Temporibus asperiores dolorem fugiat facilis tempora aliquam in praesentium, eveniet laboriosam optio.</p>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Adipisci soluta aut praesentium sint, quam excepturi.</p>
            <h5>T.Johnson <i class="fa-solid fa-quote-right"></i></h5>
          </div>
        </div>
      </div>
    </section>
</template>

<script>
import MySection4Card from './MySection4Card.vue';

export default {
    name: 'MySection4',
    components: {
      MySection4Card
    },
    data() {
      return {
        employees: [
          {
            imgSrc: require('../assets/img/team-1.jpg'),
            name: 'David Cooper',
            role: 'CTO & CO-FOUNDER'
          },
          {
            imgSrc: require('../assets/img/team-3.jpg'),
            name: 'Oliver Jones',
            role: 'CHIEF PROCUREMENT'
          },
          {
            imgSrc: require('../assets/img/team-2.jpg'),
            name: 'Emma Lopez',
            role: 'CHIEF MARKETING'
          },
          {
            imgSrc: require('../assets/img/team-4.jpg'),
            name: 'T.Johnson',
            role: 'CEO & PRESIDENT'
          },
        ]
      }
    }

}
</script>

<style scoped lang="scss">
@import '../style/vars.scss';
@import '~@fortawesome/fontawesome-free/css/all.css';

#section4 {
  background-color: $c8;
  padding: 100px 0;
  color: #fff;

  .container {
    justify-content: space-between;
  }

  .s4_left {
    flex-basis: calc(100% / 3 * 2 - 40px);
    
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

    .employee_container {
      flex-wrap: wrap;
    }
  }

  .s4_right {
    flex-basis: calc(100% / 3);

    .s4r_top {
      height: 10%;
    }

    .s4r_bottom {
      background-color: $c2;
      padding: 30px;
      border-radius: 5px;

      p {
        margin: 20px 0;
        color: $c4;
      }

      h4 {
        font-size: 1.5rem;
      }

      h5 {
        position: relative;

        i {
          position: absolute;
          right: 0;
          top: -20px;
          font-size: 2rem;
          color: $c12;
        }
      }
    }
  }
}
</style>