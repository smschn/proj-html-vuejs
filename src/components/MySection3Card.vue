<template>
    <div class="circle_card_container">
        <div class="circle">{{processProps.number}}</div>
        <h3>{{processProps.title}}</h3>
        <p>{{processProps.text}}</p>
    </div>
</template>

<script>
export default {
    name: 'MySection3Card',
    props: {
        processProps: Object
    }
}
</script>

<style scoped lang="scss">
@import '../style/vars.scss';

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
</style>