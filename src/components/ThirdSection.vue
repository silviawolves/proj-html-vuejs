<template>
    <div class="container py-5">

        <div class="row align-items-center">
            <div class="col">
                <div class="pe-2">
                    <h4 class="fw-bold pb-3">Build tools and extensive documentation</h4>
                    <p>You can combine all the Landrick templates into a single one, you can take a component from the Application theme and use it in the Website.</p>
                    <ul class="list-unstyled">
                        <li class="pb-1" v-for="(pro, i) in advantages" :key="i">
                            <i class="fa-regular fa-circle-check"></i> {{ pro.text }}
                        </li>
                    </ul>

                    <button class="my-btn blue-button">Read More <i class="fa-solid fa-arrow-right"></i></button>
                </div>
            </div>

            <div class="col">
                <img src="img/1.png" alt="schema funzionalità" class="w-75 float-end">
            </div>
        </div>

    </div>
</template>

<script>
export default {
    name: 'ThirdSection',
    data() {
        return {
            advantages: [
                {
                    text: 'Digital Marketing Solutions for Tomorrow',
                },
                {
                    text: 'Our Talented and Experienced Marketing Agency',
                },
                {
                    text: 'Create your own skin to match your brand',
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/_variables.scss";
@import "../assets/scss/button.scss";

p, ul li {
    color: $font-gray;
    font-size: .8rem;

    i {
        color: $secondary;
        margin-right: .2rem;
    }
}
</style>