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
</style>