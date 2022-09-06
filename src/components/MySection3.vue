<template>
    <section id="section3">
      <div class="container s3_first">
        <h5>how it works in practice</h5>
        <h1><span>Process</span> Management</h1>
        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Natus, reprehenderit quasi. Facilis, suscipit dolor voluptatum minima ea fugit exercitationem nam!</p>
      </div>
      <div class="s3_second">
        <div class="circle_card_container" v-for="(process, index) in processesData" v-bind:key="index">
          <div class="circle">{{process.number}}</div>
          <h3>{{process.title}}</h3>
          <p>{{process.text}}</p>
        </div>
      </div>
    </section>
</template>

<script>
export default {
    name: 'MySection3',
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

    .circle_card_container {
      flex-basis: calc(100% / 5);
      text-align: center;
      border-top: 4px solid $c4;
      position: relative;
      padding: 30px;

      .circle {
        width: 40px;
        height: 40px;
        border-radius: 50%;
        background-color: $c4;
        position: absolute;
        left: 50%;
        transform: translateX(-50%);
        top: -22px;
        text-align: center;
        line-height: 40px;
        color: $c2;
        font-weight: bold;
      }

      h3 {
        margin: 30px 0;
      }

      p {
        color: grey;
      }
    }
  }
}
</style>