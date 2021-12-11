<template>
    <div class="background-image">
        <Section/>
    </div>
</template>

<script>
import Section from '@/components/Section.vue'

export default {
    name: 'Main',

    components: {
        Section,
    }

}
</script>

<style lang="scss" scoped>
    .background-image {
        height: 700px;
        background-image: url(../assets/home-background.png);
        background-repeat: no-repeat;
        background-position: center;
    }

</style>