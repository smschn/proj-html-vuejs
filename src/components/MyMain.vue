<template>
  <main>
    <MySection1 />
    <MySection2 />
    <section id="section3">
      to do
    </section>
    <section id="section4">
      <div class="container d_flex">
        <div class="s4_left">
          <div>
            <h5>we like what we do</h5>
            <h1><span>Team</span> of Experts</h1>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dolores consequatur molestiae fugiat molestias cupiditate repellat ullam quod exercitationem odio unde.</p>
          </div>
          <div class="employee_container d_flex">
            <div class="employee_card d_flex" v-for="(employee, index) in employees" v-bind:key="index">
              <img v-bind:src="employee.imgSrc" v-bind:alt="employee.name">
              <div class="employee_info">
                <h4>{{employee.name}}</h4>
                <h6>{{employee.role}}</h6>
                <i class="fa-brands fa-facebook-f"></i>
                <i class="fa-brands fa-twitter"></i>
                <i class="fa-brands fa-linkedin-in"></i>
              </div>
            </div>
          </div>
        </div>
        <div class="s4_right">dx</div>
      </div>
    </section>
    <section id="section5"></section>
    <section id="section6"></section>
  </main>
</template>

<script>
import MySection1 from './MySection1.vue';
import MySection2 from './MySection2.vue';

export default {
    name: 'MyMain',
    components: {
      MySection1,
      MySection2
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

#section3 {
  padding: 300px;
}

#section4 {
  background-color: $c8;
  padding: 100px 0;
  color: #fff;

  .s4_left {
    flex-basis: calc(100% / 3 * 2);
    
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

    .employee_card {
      margin-top: 30px;
      flex-basis: calc(100% / 2);

      img {
        width: 80px;
        border-radius: 5px;
      }

      .employee_info {
        padding: 10px 0 0 20px;

        h6 {
          margin: 15px 0;
        }

        i {
          margin: 0 10px;
          background-color: red;
        }
      }
    }
  }

  .s4_right {
    flex-basis: calc(100% / 3);
  }
}
</style>