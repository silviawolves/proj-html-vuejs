<template>
    <div>
        <footer>
            <div class="container">

                <div class="row">
                    <div class="col">
                        <img src="img/logo-light.png" alt="logo landrick">
                        <p class="pb-1">Start working with Landrick that can provide everything you need to generate awareness, drive traffic, connect.</p>
                        <div class="social-container">
                            <button v-for="(social, i) in social" :key="i"><i :class="social.icon"></i></button>
                        </div>
                    </div>

                    <div class="col">
                        <div class="col"></div>
                        <div class="col"></div>
                    </div>

                    <div class="col">

                    </div>
                </div>

            </div>
        </footer>
    </div>
</template>

<script>
export default {
    name: 'TheFooter',
    data() {
        return {
            social: [
                {
                    name: 'Facebook',
                    icon: 'fa-brands fa-facebook-f',
                },
                {
                    name: 'Instagram',
                    icon: 'fa-brands fa-instagram',
                },
                {
                    name: 'Twitter',
                    icon: 'fa-brands fa-twitter',
                },
                {
                    name: 'Linkedin',
                    icon: 'fa-brands fa-linkedin-in',
                },
            ],
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/main.scss";
@import "../assets/scss/_variables.scss";

footer {
    background-color: $quaternary;
    padding: 2.5rem;
    color: $font-lightgray;
    font-size: .7rem;

    img {
        height: 20px;
        margin-bottom: 1rem;
    }

    button {
        border: none;
        background-color: $quaternary;
        border-radius: 15%;
        width: 30px;
        height: 30px;
        margin: .2rem;
        border: 1px solid $font-lightgray;

        &:hover {
            background-color: lighten($color: $quaternary, $amount: 20);
        }

        i {
            color: $font-lightgray;
            font-size: .7rem;
        }
    }

}

</style>