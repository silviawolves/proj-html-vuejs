<template>
    <div class="container py-3">
        <h4 class="fw-bold pb-2 text-black">Key Features</h4>
        <p>Start working with <span>Landrick</span> that can provide everything you need to generate awareness, drive traffic, connect.</p>

        <div class="row">
            <div class="col" v-for="(card, i) in keyFeatures" :key="i">

                <div class="my-card">
                    <div class="square-btn"><i class="fa-solid" :class="card.icon"></i></div>
                    <h6 class="fw-bold text-black pt-3">{{ card.title }}</h6>
                    <p class="w-100">{{ card.content }}</p>
                    <a href="javascript:void(0)">Read More <i class="fa-solid fa-chevron-right"></i></a>
                </div>

            </div>
        </div>

    </div>
</template>

<script>
export default {
    name: 'FirstSection',
    data() {
        return {
            keyFeatures: [
                {
                    icon: 'fa-layer-group',
                    title: 'Modular',
                    content: 'Composed in a pseudo-Latin language which more or less corresponds',
                },
                {
                    icon: 'fa-display',
                    title: 'Responsive',
                    content: 'Composed in a pseudo-Latin language which more or less corresponds',
                },
                {
                    icon: 'fa-arrows-to-eye',
                    title: 'Customizable',
                    content: 'Composed in a pseudo-Latin language which more or less corresponds',
                },
                {
                    icon: 'fa-maximize',
                    title: 'Scalable',
                    content: 'Composed in a pseudo-Latin language which more or less corresponds',
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/_variables.scss";
@import "../assets/scss/button.scss";
.container {
    font-size: .8rem;
    color: $font-gray;

        & > p {
            width: 50%;
            padding-bottom: 2rem;

            span {
                color: $secondary;
                font-weight: bold;
            }
        }

        .my-card {
            border: 1px solid $light-border;
            border-radius: 5px;
            padding: 1rem;

            .square-btn {
                height: 50px;
                border: none;
                display: flex;
                justify-content: center;
                align-items: center;

                i {
                    font-size: 1rem;
                    color: $secondary;
                    text-align: center;
                }
            }


            //READ MORE
            a {
                text-decoration: none;
                color: $secondary;
                font-size: .8rem;
                font-weight: bold;

                & > i {
                    font-size: .5rem;
                }

            &:hover {
                color: $tertiary;
                transition: color .3s linear;
            }

        }
    }
}

</style>