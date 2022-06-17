<template>
    <main>
        <jumbotronSection/>
        <meetSection/>
        <servicesSection/>
        <productsSection/>
        <reviewsSection/>
        <recentBlogSection/>
    </main>
</template>

<script>

import jumbotronSection from '../sections/jumbotronSection.vue'
import meetSection from '../sections/meetSection.vue'
import servicesSection from '../sections/servicesSection.vue'
import productsSection from '../sections/productsSection.vue'
import reviewsSection from '../sections/reviewsSection.vue'
import recentBlogSection from '../sections/recentBlogSection.vue'

export default {

    name: 'MainComponent',

    data() {

        return {
            
        }

    },

    components: {
        jumbotronSection,
        meetSection,
        servicesSection,
        productsSection,
        reviewsSection,
        recentBlogSection,
    }

}
</script>

<style lang="scss" scoped>


</style>