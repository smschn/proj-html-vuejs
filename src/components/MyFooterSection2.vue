<template>
    <section id="f2">
        <div class="container f2 d_flex">
            <div>
                Enjoy the low price. We are tracking any itnention of piracy.
            </div>
            <div>
                &copy; 2022 NEXGEN is Pourdly Powered by <a href="#">Codings</a>.
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'MyFooterSection2'
}
</script>

<style scoped lang="scss">
@import '../style/vars.scss';
@import '~@fortawesome/fontawesome-free/css/all.css';

#f2 {
    background-color: $c15;
    color: $c1;
    padding: 20px 0;
    font-size: 0.8rem;

    .f2 {
        justify-content: space-between;

        a {
            color: $c2;
            text-decoration: none;
        }
    }
}
</style>