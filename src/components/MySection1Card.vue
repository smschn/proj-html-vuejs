<template>
    <div class="square">
        <i v-bind:class="squareProps.iconClass"></i>
        <h2>{{squareProps.title}}</h2>
        <p>{{squareProps.text}}</p>
    </div>
</template>

<script>
export default {
    name: 'MySection1Card',
    props: {
        squareProps: Object
    }
}
</script>

<style scoped lang="scss">
@import '../style/vars.scss';

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
</style>