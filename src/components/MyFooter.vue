<template>
    <footer>
        <section id="f1">
            <div class="container f1 d_flex">
                <div class="card_footer">
                    <div class="d_flex logo">
                        <span class="logo_left">NEX</span>
                        <span class="logo_right">GEN</span>
                    </div>
                    <ul>
                        <li>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Et, itaque.</li>
                        <li><i class="fa-solid fa-phone"></i> +1 (305) 1234-5678</li>
                        <li><i class="fa-solid fa-envelope"></i> hello@example.com</li>
                        <li><i class="fa-sharp fa-solid fa-location-dot"></i> Main Avenue, 987</li>
                    </ul>
                    <button>get in touch</button>
                </div>
                <div class="card_footer">
                    <h2>about</h2>
                    <ul>
                        <li>> item</li>
                        <li>> item</li>
                        <li>> item</li>
                        <li>> item</li>
                        <li>> item</li>

                    </ul>
                </div>
                <div class="card_footer">services</div>
                <div class="card_footer">support</div>

            </div>
        </section>
        <section id="f2"></section>
    </footer>
</template>

<script>
export default {
    name: 'MyFooter'
}
</script>

<style scoped lang="scss">
@import '../style/vars.scss';
@import '~@fortawesome/fontawesome-free/css/all.css';

#f1 {
    padding: 100px 0;
    background-color: $c13;
    color: $c1;

    li {
        list-style: none;
    }

    .container.f1 {
        justify-content: space-between;

        .card_footer {
            flex-basis: calc(100% / 4 - 10px);

            .logo {
                font-weight: bold;
                letter-spacing: 5px;

                .logo_left {
                    border-top-left-radius: 20px;
                    border-bottom-left-radius: 20px;
                    background-color: $c12;
                    padding: 10px 1px 10px 20px;
                    color: $c5;
                    margin-right: 2px;
                }

                .logo_right {
                    line-height: 38px;
                }
            }
        }

        .card_footer:first-child {

            ul li {
                margin: 15px 0;
            }
        }

        .card_footer:nth-child(2),
        .card_footer:nth-child(3),
        .card_footer:nth-child(4) {
            background-color: red;
        }

    }
}
</style>