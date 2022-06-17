<template>
    <div class="featured-card">
        <img :src="require('@/assets/img/' + featuredCard.img + '')" :alt="featuredCard.img">
        <div class="text-area">
            <div class="uptext">{{featuredCard.uptext}}</div>
            <h2>{{featuredCard.title}}</h2>
            <p>{{featuredCard.description}}</p>
            <mainButton class="button" :button="button"/>
        </div>
        
    </div>
</template>

<script>

import mainButton from '../nano-components/mainButton.vue'

export default {

    name: 'featuredCard',

    data() {
        return {
            button: {
                text: 'BUY NOW',
                link: '#',
            },
        }
    },

    components: {
        mainButton,
    },

    props: {
        featuredCard: Object,
    }

}

</script>

<style lang="scss" scoped>

.featured-card {
    display: flex;
    border: none;
    background: var(--dark-bg);
    max-width: var(--main-container-width);
    border-top: 4px solid var(--primary-color);
    max-height: 456px;
}

img {
    max-width: 456px;
    background-image: url(../assets/img/avadabarbers-cta-background.jpg);
    background-position: center;
    background-size: cover;
}

.text-area {
    display: flex;
    flex-direction: column;
    padding: 70px 70px 0;
    overflow-y: auto;
}

.uptext {
    color: var(--primary-color);
    font-weight: 700;
}

h2 {
    color: var(--secondary-color);
}

p {
    color: var(--secondary-color);
    font-size: 1.125rem;
    margin-bottom: 30px;
}

</style>