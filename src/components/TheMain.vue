<template>
    <div>
        
        <FirstSection></FirstSection>
        <SecondSection></SecondSection>
        <ThirdSection></ThirdSection>

    </div>
</template>

<script>
import FirstSection from './FirstSection.vue';
import SecondSection from './SecondSection.vue';
import ThirdSection from './ThirdSection.vue';

export default {
    name: "TheMain",
    components: { FirstSection, SecondSection, ThirdSection },
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/main.scss";
@import "../assets/scss/_variables.scss";

</style>