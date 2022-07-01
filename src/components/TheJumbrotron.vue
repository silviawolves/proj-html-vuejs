<template>
    <div class="jumbotron">
        <div class="row align-items-center justify-content-center">

            <!--CONTENUTO TESTUALE-->
            <div class="col">
                <button>Development</button>
                <h1>A Complete Developer Toolset</h1>
                <p>Launch your campaign and benefit from our expertise on designing and managing conversion centered bootstrap4 html page.</p>
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

.jumbotron {
    padding: 4rem 0;

    button {
        border: none;
        border-radius: 50px;
        background-color: $btn-grey;
        border: 1px solid $btn-grey;
        color: $secondary;
        font-size: .6rem;
        font-weight: bold;
        margin-bottom: 1rem;
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