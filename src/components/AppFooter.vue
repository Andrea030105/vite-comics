<script>
import digitalComics from '../assets/images/buy-comics-digital-comics.png'
import merchandise from '../assets/images/buy-comics-merchandise.png'
import subscriptions from '../assets/images/buy-comics-subscriptions.png'
import shopLocator from '../assets/images/buy-comics-shop-locator.png'
import dcPowerVisa from '../assets/images/buy-dc-power-visa.svg'
export default {
    data() {
        return {
            commerceMenu: [
                {
                    icon: digitalComics,
                    text: 'digital comics',
                },
                {
                    icon: merchandise,
                    text: 'merchandise',
                },
                {
                    icon: subscriptions,
                    text: 'subscriptions',
                },
                {
                    icon: shopLocator,
                    text: 'shop locator',
                },
                {
                    icon: dcPowerVisa,
                    text: 'dc power visa',
                },
            ],
            footerMenu: [
                {
                    title: 'DC Comics',
                    links: [
                        'Characters',
                        'Comics',
                        'Movies',
                        'TV',
                        'Games',
                        'Videos',
                        'News'
                    ]
                },
                {
                    title: 'Shop',
                    links: [
                        'Shop DC',
                        'Shop DC Collectibles'
                    ]
                },
                {
                    title: 'DC',
                    links: [
                        'Terms Of Use',
                        'Privacy Policy',
                        'Ad Choices',
                        'Advertising',
                        'Jobs',
                        'Subscriptions'
                    ]
                },
                {
                    title: 'SITE',
                    links: [
                        'Dc',
                        'Mad Magazine',
                        'Dc Kids',
                        'Dc Universe',
                        'Dc Power Vista'
                    ]
                }
            ]
        }
    },
}
</script>
<template>
    <section class="bg-primary">
        <div class="container">
            <div class="row">
                <div class="col-12">
                    <div class="d-flex justify-content-between p-4">
                        <div class="commerce-card d-flex align-items-center" v-for="(items, index) in commerceMenu"
                            :key="index">
                            <img :src="items.icon" :alt="items.text">
                            <p>{{ items.text }}</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <section class="link-section">
        <div class="container">
            <div class="row">
                <div class="col-2 pt-4">
                    <div class="link-card" v-for="(items, index) in footerMenu.slice(0, 2)" :key="index">
                        <h4>
                            {{ items.title }}
                        </h4>
                        <ul>
                            <li v-for="(link, i) in items.links" :key="i">
                                <a href="#">
                                    {{ link }}
                                </a>
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="col-10 pt-4 d-flex">
                    <div class="link-card me-5" v-for="(items, index) in footerMenu.slice(2)" :key="index">
                        <h4>
                            {{ items.title }}
                        </h4>
                        <ul>
                            <li v-for="(link, i) in items.links" :key="i">
                                <a href="#">
                                    {{ link }}
                                </a>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
<style lang="scss">
@use '../styles/partial/variables' as *;

.commerce-card {
    img {
        width: 40px;
        height: 45px;
    }

    p {
        margin-bottom: 0;
        margin-left: 1rem;
        color: $whiteCl;
        text-transform: uppercase;
    }
}

.link-section {
    background-image: url('../assets/images/dc-logo-bg.png'), url('../assets/images/footer-bg.jpg');
    background-position:
        right center,
        top left;
    background-repeat:
        no-repeat,
        repeat;
}

.link-card {
    h4 {
        color: $whiteCl;
        font-weight: 600;
        text-transform: uppercase;
    }

    a {
        color: $grayCl;

        &:hover {
            text-decoration: underline !important;
            color: $whiteCl;
        }
    }

}
</style>