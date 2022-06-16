<template>
    <main>
        <jumbotronSection/>
        <meetSection/>
    </main>
</template>

<script>

import jumbotronSection from '../micro-components/jumbotronSection.vue'
import meetSection from '../micro-components/meetSection.vue'

export default {

    name: 'MainComponent',

    data() {

        return {
            
        }

    },

    components: {
        jumbotronSection,
        meetSection,
    }

}
</script>

<style lang="scss" scoped>


</style>