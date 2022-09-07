<template>
    <div class="card_footer">
        <h2>{{cardProps.title}}</h2>
        <ul>
            <li v-for="(link2, index2) in cardProps.links" v-bind:key="index2"><a v-bind:href="link2.url"><i class="fa-solid fa-angle-right"></i> {{link2.text}}</a></li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'MyFooterSection1Card',
    props: {
        cardProps: Object
    }
}
</script>

<style scoped lang="scss">
@import '../style/vars.scss';

li {
    list-style: none;
    margin: 12px 0;
}

h2 {
    color: #fff;
    margin-bottom: 20px;
}

a {
    text-decoration: none;
    color: $c1;
}
</style>