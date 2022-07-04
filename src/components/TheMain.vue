<template>
    <div>
        
        <FirstSection></FirstSection>
        <SecondSection></SecondSection>

    </div>
</template>

<script>
import FirstSection from './FirstSection.vue';
import SecondSection from './SecondSection.vue';

export default {
    name: "TheMain",
    components: { FirstSection, SecondSection },
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/main.scss";
@import "../assets/scss/_variables.scss";

</style>