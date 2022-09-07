<template>
    <div class="news_card d_flex">
        <img v-bind:src="newsProps.imgSrc" v-bind:alt="newsProps.alt">
        <p>{{newsProps.text}}</p>
    </div>
</template>

<script>
export default {
    name: 'MySection5Card',
    props: {
        newsProps: Object
    }
}
</script>

<style scoped lang="scss">
.news_card {
      flex-basis: calc(100% / 3 - 5px);
      max-height: 340px;
      margin-top: 30px;
      border-radius: 10px;
      position: relative;
      justify-content: center;

      img {
        max-width: 100%;
        max-height: 100%;
        filter: brightness(50%);
        border-radius: 10px;
      }

      p {
        position: absolute;
        bottom: 20%;
        text-align: center;
        max-width: 70%;
      }
}
</style>