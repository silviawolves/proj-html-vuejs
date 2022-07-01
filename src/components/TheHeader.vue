<template>
    <div class="container">
        <div class="d-flex justify-content-between">

            <!--LOGO PAGINA-->
            <div class="page-logo">
                <img src="/img/logo-dark.png" alt="logo landrick">
            </div>

            <!--LINK DI NAVIGAZIONE-->
            <div class="page-navlink">
                <ul class="list-unstyled d-flex">
                    <li v-for="(link, i) in navLinks" :key="i"><a href="javascript:void(0)">{{ link }}</a></li>
                </ul>
            </div>

            <!--FEATURES-->
            <div class="page-features">
                <i class="fa-solid fa-magnifying-glass"></i>
                <button v-for="btn in features" :key="btn.name" class="btn btn-primary">
                    <i :class="btn.icon"></i>
                </button>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'TheHeader',
    data() {
        return {
            navLinks: ['Home', 'Landing', 'Pages', 'Docs'],
            features: [
                {
                    name: 'GitHub',
                    icon: 'fa-brands fa-github',
                },
                {
                    name: 'Stack Overflow',
                    icon: 'fa-brands fa-stack-overflow',
                },
                {
                    name: 'User',
                    icon: 'fa-regular fa-user',
                }
            ],
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/main.scss";
@import "../assets/scss/_variables.scss";

.page-logo img {
    height: 20px;
}

</style>