<template>
    <div class="wrapper">
        <footer>
            <div class="container">

                <!--SOMMARIO LANDRICK + SOCIAL-->
                <div class="row">
                    <div class="col">
                        <img src="img/logo-light.png" alt="logo landrick">
                        <p class="pb-1">Start working with Landrick that can provide everything you need to generate awareness, drive traffic, connect.</p>
                        <div class="social-container">
                            <button class="square-btn" v-for="(social, i) in social" :key="i"><i :class="social.icon"></i></button>
                        </div>
                    </div>

                    <!--COLONNE CON LINK INTERNI AL SITO-->
                    <div class="col">
                        <div class="row">
                            <div class="col">
                                <h6 class="fw-bold text-white pb-2">Company</h6>
                                <ul class="list-unstyled m-0">
                                    <li v-for="(link, i) in companyLinks" :key="i">
                                    <i class="fa-solid fa-chevron-right"></i><a href="javascript:void(0)"> {{ link }}</a></li>
                                </ul>
                            </div>

                            <div class="col">
                                <h6 class="fw-bold text-white pb-2">Useful Links</h6>
                                <ul class="list-unstyled m-0">
                                    <li v-for="(link, i) in usefulLinks" :key="i">
                                    <i class="fa-solid fa-chevron-right"></i><a href="javascript:void(0)"> {{ link }}</a></li>
                                </ul>
                            </div>
                        </div>
                    </div>

                    <!--ISCRIZIONE NEWSLETTER-->
                    <div class="col-3">
                        <h6 class="fw-bold text-white pb-3">Newsletter</h6>
                        <p>Subscribe and receive the latest tips via email.</p>
                        <div class="fw-bold pb-1">Write your email <span class="asterisk-sign">*</span></div>

                        <div class="form-floating">
                            <input type="email" class="form-control" id="floatingInput" placeholder="name@example.com">
                            <label for="floatingInput"><i class="fa-regular fa-envelope me-2"></i> Your email:</label>
                            
                            <button class="sub-btn">Subscribe</button>
                        </div>
                    </div>
                </div>

            </div>
        </footer>

        <LowerFooter></LowerFooter>
        
        <!--BOTTONE CHE SCROLLA IN CIMA ALLA PAGINA-->
        <button class="scroll-btn square-btn" @click="toTheTop()"><i class="fa-solid fa-arrow-up"></i></button>
    </div>
</template>

<script>
import LowerFooter from './LowerFooter.vue'

export default {
    name: "TheFooter",
    components: { LowerFooter },
    data() {
        return {
            social: [
                {
                    name: "Facebook",
                    icon: "fa-brands fa-facebook-f",
                },
                {
                    name: "Instagram",
                    icon: "fa-brands fa-instagram",
                },
                {
                    name: "Twitter",
                    icon: "fa-brands fa-twitter",
                },
                {
                    name: "Linkedin",
                    icon: "fa-brands fa-linkedin-in",
                },
            ],
            companyLinks: ["About us", "Services", "Team", "Pricing", "Project", "Careers", "Blog", "Login"],
            usefulLinks: ["Terms of Services", "Privacy Policy", "Documentation", "Changelog", "Components"],
        };
    },
    methods: {
        toTheTop() {
            window.scrollTo(0, 0);
        }
    },
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/_variables.scss";
@import "../assets/scss/button.scss";

.wrapper {
    position: relative;

    footer {
        background-color: $quaternary;
        padding: 2.5rem 0;
        color: $font-lightgray;
        font-size: .8rem;
        border-bottom: 1px solid #27314f;

        img {
            height: 20px;
            margin-bottom: 1.5rem;
        }

        .square-btn {
            background-color: $quaternary;
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

        //LINKS SECTION - II, III COL
        li {
            padding-top: .5rem;

            i {
                font-size: .4rem;
                margin-right: .5rem;
                vertical-align: middle;
            }

            a {
                text-decoration: none;
                color: $font-lightgray;
            }
        }
        
        //NEWSLETTER SECTION - IV COL
        .asterisk-sign {
            color: $reddish;
        }

        .form-floating > .form-control {
            height: 20px;
        }
        .form-control {
            background-color: #27314f;
            border: none;
        }

        .form-floating > label {
            padding: .35rem 1rem;
            height: auto;
        }

        .sub-btn {
            width: 100%;
            background-color: #27314f;
            color: $secondary;
            font-size: .8rem;
            font-weight: bold;
            border: none;
            border-radius: 5px;
            padding: .5rem;
            margin-top: 1rem;
            box-shadow: 0px 2px 5px $tertiary;

            &:hover {
                background-color: lighten($color: #27314f, $amount: 5);
                color: $font-lightgray;
            }
        }
    }
    .scroll-btn {
        background-color: transparent;
        width: 30px;
        height: 30px;
        position: fixed;
        right: 20px;
        bottom: 20px;
        line-height: 35%;
        
            i {
                color: $font-lightgray;
                font-size: .7rem;
            }

            &:hover {
                background-color: $tertiary;
                    
                i {
                    color: white;
                }
            }
    }
}
</style>