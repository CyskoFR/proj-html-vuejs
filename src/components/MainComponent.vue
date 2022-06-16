<template>
    <main>
        <jumbotronSection/>
        <meetSection/>
        <servicesSection/>
        <productsSection/>
    </main>
</template>

<script>

import jumbotronSection from '../sections/jumbotronSection.vue'
import meetSection from '../sections/meetSection.vue'
import servicesSection from '../sections/servicesSection.vue'
import productsSection from '../sections/productsSection.vue'

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
    }

}
</script>

<style lang="scss" scoped>


</style>