<template>
    <div class="services_card">
        <i v-bind:class="servicesCardProps.iconClass"></i>
        <h3>{{servicesCardProps.title}}</h3>
        <p>{{servicesCardProps.text}}</p>
        <i class="fa-solid fa-arrow-right"></i>
    </div>
</template>

<script>
export default {
    name: 'MySection2Card',
    props: {
        servicesCardProps: Object
    }
}
</script>

<style scoped lang="scss">
@import '../style/vars.scss';

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
</style>