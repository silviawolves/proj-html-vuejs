<template>
    <div class="jumbotron">
        <div class="row align-items-center justify-content-center">

            <!--CONTENUTO TESTUALE-->
            <div class="col">
                <span class="tag">Development</span>

                <h1>A Complete Developer Toolset</h1>
                <p class="pb-2">Launch your campaign and benefit from our expertise on designing and managing conversion centered bootstrap4 html page.</p>

                <button class="my-btn blue-button">Get Started</button>
                <button class="my-btn outline-btn">Documentation</button>

                <p class="mt-2"><small>Current Version: v2.6.0</small></p>
            </div>

            <!--IMMAGINE JUMBO-->
            <div class="col">
                <img src="img/about.png" alt="jumbotron image">
            </div>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@import "../assets/scss/_variables.scss";
@import "../assets/scss/button.scss";

.jumbotron {
    padding: 4rem 0;

    .tag {
        border: none;
        border-radius: 50px;
        background-color: $btn-grey;
        border: 1px solid $btn-grey;
        color: $secondary;
        font-size: .6rem;
        font-weight: bold;
        margin-bottom: 1rem;
        padding: .1rem .2rem;
    }

    h1 {
        font-weight: bold;
        line-height: 60px;
    }

    p {
        color: $font-gray;
        font-size: .9rem;
    }
}
</style>