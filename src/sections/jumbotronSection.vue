<template>
    <div class="bg">
        <div class="container">
            <div class="row w-100">
                <div class="col-6 col-text">
                    <h1>Barber Shop</h1>
                    <hr>
                    <p>The Pinnacle of Male Grooming</p>
                    <mainButton :button="jumboButton"/>
                </div>
                <div class="col-6 col-img">
                    <img class="jumbo_img" src="../assets/img/avadabarbers_hero_focalmirror-600x825.png" alt="">
                </div>
            </div>
            
        </div>
    </div>
</template>

<script>

import mainButton from '../nano-components/mainButton.vue'

export default {

    name: 'jumbotronSection',

    data() {
        return {
            jumboButton: {
                text: 'LEARN MORE',
                link: '#',
            }
        }
    },

    components: {
        
        mainButton,

    }

}

</script>

<style lang="scss" scoped>

.bg {
    width: 100%;
    background-image: url(../assets/img/avadabarbers-homepage-hero-bg.jpg);
    background-position: top;
    background-size: cover;
}

.container {
    display: flex;
    align-items: center;
    width: var(--main-container-width);
    min-height: 960px;
}

.col-text {
    display: flex;
    flex-direction: column;
    justify-content: center;

    h1 {
        color: white;
        font-size: 4.5rem;
    }

    hr {
        height: 4px;
        width: 38%;
        background-color: var(--primary-color);
        opacity: 1;
        margin: 0;
        margin-bottom: var(--main-margin-y);
    }

    p {
        color: grey;
        font-size: 1.25rem;
        margin-bottom: 35px;
    }
}

.jumbo_img {
    width: 100%;
}

</style>