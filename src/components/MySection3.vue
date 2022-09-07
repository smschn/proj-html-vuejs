<template>
    <section id="section3">
      <div class="container s3_first">
        <h5>how it works in practice</h5>
        <h1><span>Process</span> Management</h1>
        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Natus, reprehenderit quasi. Facilis, suscipit dolor voluptatum minima ea fugit exercitationem nam!</p>
      </div>
      <div class="s3_second">
        <MySection3Card v-for="(process, index) in processesData" v-bind:key="index" :processProps="process" />
      </div>
    </section>
</template>

<script>
import MySection3Card from './MySection3Card.vue';

export default {
    name: 'MySection3',
    components: {
      MySection3Card
    },
    data() {
      return {
        processesData: [
          {
            number: '01',
            title: 'Collection of information',
            text: 'Lorem ipsum dolor sit amet consectetur adipisicing.'
          },
          {
            number: '02',
            title: 'Strategic planning',
            text: 'Lorem ipsum dolor sit amet consectetur adipisicing.'
          },
          {
            number: '03',
            title: 'Assignment of responsibilities',
            text: 'Lorem ipsum dolor sit amet consectetur adipisicing.'
          },
          {
            number: '04',
            title: 'Formatting process',
            text: 'Lorem ipsum dolor sit amet consectetur adipisicing.'
          },
          {
            number: '05',
            title: 'Continuity formalization',
            text: 'Lorem ipsum dolor sit amet consectetur adipisicing.'
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
  padding: 100px;

  .container.s3_first {
    text-align: center;

    h5 {
      text-transform: uppercase;
      color: $c5;
    }

    h1 {
      margin: 20px 0;
      font-size: 3rem;

      span {
      background-color: $c4;
      color: $c2;
      border-radius: 5px;
      padding: 10px;
      }
    }

    p {
      color: grey;
    }
  }

  .s3_second {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    margin-top: 50px;
  }
}
</style>