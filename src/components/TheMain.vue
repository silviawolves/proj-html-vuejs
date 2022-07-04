<template>
    <div class="container py-5">
        
        <FirstSection></FirstSection>

    </div>
</template>

<script>
import FirstSection from './FirstSection.vue';

export default {
    name: "TheMain",
    components: { FirstSection },
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/main.scss";
@import "../assets/scss/_variables.scss";

</style>