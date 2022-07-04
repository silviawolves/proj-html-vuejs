<template>
    <div>
        
        <FirstSection></FirstSection>
        <SecondSection></SecondSection>
        <ThirdSection></ThirdSection>
        <FourthSection></FourthSection>
        <FifthSection></FifthSection>

    </div>
</template>

<script>
import FirstSection from './FirstSection.vue';
import SecondSection from './SecondSection.vue';
import ThirdSection from './ThirdSection.vue';
import FourthSection from './FourthSection.vue';
import FifthSection from './FifthSection.vue';

export default {
    name: "TheMain",
    components: { FirstSection, SecondSection, ThirdSection, FourthSection, FifthSection },
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/main.scss";

</style>