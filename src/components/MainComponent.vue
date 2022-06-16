<template>
    <main>
        <jumbotronSection/>
        <meetSection/>
        <servicesSection/>
    </main>
</template>

<script>

import jumbotronSection from '../sections/jumbotronSection.vue'
import meetSection from '../sections/meetSection.vue'
import servicesSection from '../sections/servicesSection.vue'

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
    }

}
</script>

<style lang="scss" scoped>


</style>