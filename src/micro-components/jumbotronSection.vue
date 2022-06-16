<template>
    <div class="jumbo_bg">
        <div class="jumbo_container container">
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
            }
        }
    },

    components: {
        
        mainButton,

    }

    

}

</script>

<style lang="scss" scoped>

.jumbo_bg {
    width: 100%;
    background-image: url(../assets/img/avadabarbers-homepage-hero-bg.jpg);
    background-position: top;
    background-size: cover;
}

.jumbo_container {
    display: flex;
    align-items: center;
    width: var(--main-container-width);
    height: 1080px;
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
        margin: 35px 0;
    }

    p {
        color: grey;
        font-size: 1.25rem;
        font-weight: 200;
        margin-bottom: 35px;
    }
}

.jumbo_img {
    width: 100%;
}

</style>