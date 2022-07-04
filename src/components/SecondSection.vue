<template>
    <div class="container py-4">

        <div class="row justify-content-center text-center">
            <div class="col-6">
                <div class="quickstart">Quickstart</div>
                <h4 class="fw-bold">Awesome isn't it? Let's dive in!</h4>
                <p>Start working with <span>Landrick</span> that can provide everything you need to generate awareness, drive traffic, connect.</p>
            </div>
        </div>

        <div class="row justify-content-center">
            <div class="col-8">
                <div class="code-table">
                    
                    <div class="code-navbar">
                        <div class="code-btn" v-for="(command, i) in codeSection" :key="i">
                            <a href="javascript:void(0)">{{ command }}</a>
                        </div>
                    </div>

                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SecondSection',
    data() {
        return {
            codeSection: ['npm', 'nuget', 'spm', 'github']
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/_variables.scss";

.quickstart, p > span {
    color: $secondary;
}

.quickstart, p {
    font-size: .8rem;
}

p {
    color: $font-gray;
}

.code-table {
    background-color: $slate-gray;
    padding: .5rem;
    border-radius: 5px;

    .code-navbar {
        background-color: #4f5a69;
        border-radius: 5px;
        margin: .5rem;
        text-align: center;
        display: flex;

        .code-btn {
            width: calc(100% / 4);
            height: 100%;
            border-radius: 5px;

            a {
                height: 100%;
                color: white;
                text-decoration: none;
                font-weight: bold;
                padding: .2rem 2.5rem;
                display: block;
                border-radius: 5px;
                border: .5px solid #4f5a69;

                &:focus {
                    background-color: $slate-gray;
                    border: .5px solid #576272;
                }
            }
        }
    }
}

</style>