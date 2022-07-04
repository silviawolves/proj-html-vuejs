<template>
    <div>
        <div class="my-card">
            <div class="plan-nametag">{{ planTag }}</div>
            <h3 class="fw-bold pt-4 text-black mb-1">{{ planPrice }}</h3>
            <div>{{ planRep }}</div>
            <p class="pt-2 pb-3 border-bottom">{{ planDesc }}</p>
            <ul class="list-unstyled">
                <li class="pb-1" v-for="(el, i) in planDetails" :key="i"><i class="fa-regular fa-circle-check"></i> {{ el }}</li>
            </ul>
            <button class="my-btn blue-button">Buy Now</button>
            <p class="mb-0 pt-2">* No credit card required</p>
        </div>
    </div>
</template>

<script>

export default {
    name: 'MyCard',
    props: {
        planTag: String,
        planPrice: String,
        planRep: String,
        planDesc: String,
        planDetails: Array,
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/_variables.scss";
@import "../assets/scss/button.scss";

.my-card {
    border-bottom: 3px solid $font-lightgray;
    border-radius: 10px;
    box-shadow: 0px 0px 1px 1px $light-border;
    padding: 1rem;
    transition: transform .3s linear;
    position: relative;
    overflow: hidden;
    font-size: .8rem;
    color: $font-gray;
    transition: border-bottom .5s, transform .5s, box-shadow .5s;

    .plan-nametag {
        background-color: $btn-grey;
        font-size: .8rem;
        color: $secondary;
        font-weight: bold;
        padding: .4rem 1rem;
        border-radius: 25px;
        border: 1px solid $btn-grey;
        display: inline-block;
    }

    li i {
        color: $secondary;
        margin-right: .2rem;
    }

    button {
        margin: 0;
        display: block;
        width: 100%;
    }

    &:hover {
        transform: scale(1.05);
        border-bottom: 3px solid $secondary;
        box-shadow: 0px 5px 10px $font-lightgray;
    }
}
</style>