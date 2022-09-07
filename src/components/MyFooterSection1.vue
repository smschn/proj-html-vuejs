<template>
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
                <button class="btn">get in touch</button>
            </div>
            <div class="card_footer" v-for="(card, index) in footerCards" v-bind:key="index">
                <h2>{{card.title}}</h2>
                <ul>
                    <li v-for="(link2, index2) in card.links" v-bind:key="index2"><a v-bind:href="link2.url"><i class="fa-solid fa-angle-right"></i> {{link2.text}}</a></li>
                </ul>
            </div>
        </div>
    </section>
</template>

<script>

export default {
    name: 'MyFooterSection1',
    data() {
        return {
            footerCards: [
                {
                    title: 'About',
                    links: [
                        {
                            text: 'The Company',
                            url: '#'
                        },
                        {
                            text: 'Insitutional',
                            url: '#'
                        },
                        {
                            text: 'Social & Events',
                            url: '#'
                        },
                        {
                            text: 'Innovation',
                            url: '#'
                        },
                        {
                            text: 'Environment',
                            url: '#'
                        },
                        {
                            text: 'Technology',
                            url: '#'
                        }
                    ]
                },
                {
                    title: 'Services',
                    links: [
                        {
                            text: 'Audit & Assurance',
                            url: '#'
                        },
                        {
                            text: 'Financial Advisory',
                            url: '#'
                        },
                        {
                            text: 'Analytics M&A',
                            url: '#'
                        },
                        {
                            text: 'Middle Marketing',
                            url: '#'
                        },
                        {
                            text: 'Legal Consulting',
                            url: '#'
                        },
                        {
                            text: 'Regulatory Risk',
                            url: '#'
                        }
                    ]
                },
                {
                    title: 'Support',
                    links: [
                        {
                            text: 'Responsibility',
                            url: '#'
                        },
                        {
                            text: 'Terms of Use',
                            url: '#'
                        },
                        {
                            text: 'About Cookies',
                            url: '#'
                        },
                        {
                            text: 'Privacy Policy',
                            url: '#'
                        },
                        {
                            text: 'Accessibility',
                            url: '#'
                        },
                        {
                            text: 'Information',
                            url: '#'
                        }
                    ]
                },

            ]
        }
    }
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

    .container.f1 {
        justify-content: space-between;

        .card_footer {
            flex-basis: calc(100% / 4 - 40px);
            border-radius: 5px;

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
                    line-height: 44px;
                }
            }
        }

        .card_footer:first-child {

            div {
                font-size: 1.3rem;
            }

            ul li {
                margin: 15px 0;
            }

            button {
                margin-top: 10px;
                background-color: $c13;
                color: #fff;
                text-transform: uppercase;
            }
        }

        .card_footer:nth-child(2),
        .card_footer:nth-child(3),
        .card_footer:nth-child(4) {
            background-color: $c14;
            padding: 30px;
        }

    }
}
</style>