<template>
    <div class="container py-5 text-center">
        <div class="row justify-content-center">
            <div class="col-6">
                <h4 class="fw-bold pb-3">Want to be among the first to find out?</h4>
                <p>Start working with <span>Landrick</span> that can provide everything you need to generate awareness, drive traffic, connect.</p>

                <div class="my-input">
                    <input type="text" placeholder="Email Address" class="">
                    <button class="my-btn blue-button" type="button">Get Started</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'FifthSection',
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/_variables.scss";
@import "../assets/scss/button.scss";

p {
    color: $font-gray;
    font-size: .8rem;
    padding-bottom: 1rem;

    span {
        color: $secondary;
    }
}

.my-input {
    position: relative;

    input {
        border-radius: 25px;
        font-size: .8rem;
        color: $font-gray;
        border: 1px solid $light-border;
        padding: .6rem 1.5rem;
        width: 100%;
    }

    button {
        position: absolute;
        right: 5px;
        top: 4px;
        bottom: 4px;
        border-radius: 25px;
        margin-right: 0;
    }
}
</style>