<template>
  <main>
    <MySection1 />
    <MySection2 />
    <section id="section3">
      to do
    </section>
    <MySection4 />
    <!-- <section id="section4">
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
                <i class="fa-brands fa-facebook-f icon-background"></i>
                <i class="fa-brands fa-twitter"></i>
                <i class="fa-brands fa-linkedin-in"></i>
              </div>
            </div>
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
    </section> -->
    <section id="section5"></section>
    <section id="section6"></section>
  </main>
</template>

<script>
import MySection1 from './MySection1.vue';
import MySection2 from './MySection2.vue';
import MySection4 from './MySection4.vue';


export default {
    name: 'MyMain',
    components: {
      MySection1,
      MySection2,
      MySection4
    }
}
</script>

<style scoped lang="scss">
@import '../style/vars.scss';
@import '~@fortawesome/fontawesome-free/css/all.css';

#section3 {
  padding: 300px;
}
</style>