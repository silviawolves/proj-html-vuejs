<template>
    <div>
        <footer>
            <div class="container">

                <!--SOMMARIO LANDRICK + SOCIAL-->
                <div class="row">
                    <div class="col">
                        <img src="img/logo-light.png" alt="logo landrick">
                        <p class="pb-1">Start working with Landrick that can provide everything you need to generate awareness, drive traffic, connect.</p>
                        <div class="social-container">
                            <button v-for="(social, i) in social" :key="i"><i :class="social.icon"></i></button>
                        </div>
                    </div>

                    <!--COLONNE CON LINK INTERNI AL SITO-->
                    <div class="col">
                        <div class="row">
                            <div class="col">
                                <h6 class="fw-bold text-white pb-2">Company</h6>
                                <ul class="list-unstyled">
                                    <li v-for="(link, i) in companyLinks" :key="i">
                                    <i class="fa-solid fa-chevron-right"></i> {{ link }}</li>
                                </ul>
                            </div>

                            <div class="col">
                                <h6 class="fw-bold text-white pb-2">Useful Links</h6>
                                <ul class="list-unstyled">
                                    <li v-for="(link, i) in usefulLinks" :key="i">
                                    <i class="fa-solid fa-chevron-right"></i> {{ link }}</li>
                                </ul>
                            </div>
                        </div>
                    </div>

                    <!--ISCRIZIONE NEWSLETTER-->
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
            companyLinks: [ 'About us', 'Services', 'Team', 'Pricing', 'Project', 'Careers', 'Blog', 'Login' ],
            usefulLinks: [ 'Terms of Services', 'Privacy Policy', 'Documentation', 'Changelog', 'Components' ],
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
        width: 25px;
        height: 25px;
        margin: .1rem;
        border: 1px solid $font-lightgray;

        &:hover {
            background-color: lighten($color: $quaternary, $amount: 20);
        }

        i {
            color: $font-lightgray;
            font-size: .7rem;
        }
    }

    li {
        padding-bottom: .5rem;

        i {
            font-size: .4rem;
            margin-right: .5rem;
            vertical-align: middle;
        }
    }
}
</style>