<template>
    <div class="lower-footer">
        <div class="container d-flex justify-content-between align-items-center">

            <div class="copyright">
                <i class="fa-regular fa-copyright"></i> 2020 Landrick. Design with <i class="fa-solid fa-heart"></i> by Shreethemes.
            </div>

            <div class="payments">
                <img v-for="(img, i) in paymentMethods" :key="i"
                :src="'img/' + img.url" :alt="'Icona di' + img.name">
            </div>

        </div>
    </div>
</template>

<script>
export default {
    name: 'LowerFooter',
    data() {
        return {
            paymentMethods: [
                {
                    name: 'American Express',
                    url: 'american-ex.png',
                },
                {
                    name: 'Discover',
                    url: 'discover.png',
                },
                {
                    name: 'MasterCard',
                    url: 'master-card.png',
                },
                {
                    name: 'PayPal',
                    url: 'paypal.png',
                },
                {
                    name: 'Visa',
                    url: 'visa.png',
                },
            ]
        }
    },
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/_variables.scss";

.lower-footer {
    background-color: $quaternary;
    padding: 1.5rem;
    position: relative;

    .copyright {
        color: $font-lightgray;
        font-size: .8rem;

        .fa-heart {
            color: $reddish;
        }
    }
    .payments > img {
        height: 20px;
        margin-left: .2rem;
    }
}
</style>