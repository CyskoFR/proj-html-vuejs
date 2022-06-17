<template>
    <div class="bg">
        <div class="container-fluid">
            <div class="uptext">WE HAVE YOU COVERED</div>
            <h2>Avada Grooming Products</h2>
            <div class="row">
                <productsCard class="col" :card="card" v-for="card in cards" :key="card.name"></productsCard>
            </div>
            <mainButton class="button" :button="button"/>
        </div>
        <div class="featured_section">
            <featuredCard :featuredCard="featuredCard" :key="featuredCard.title"/>
        </div>
    </div>
</template>

<script>

import mainButton from '../nano-components/mainButton.vue'
import productsCard from '../micro-components/productsCard.vue'
import featuredCard from '../micro-components/featuredCard.vue'

export default {

    name: 'productsSection',

    data() {
        return {
            button: {
                text: 'SHOP OUR PRODUCT RANGE',
                link: '#',
            },
            cards: [
                {
                    name: 'obj-1',
                    img: "brush_dark-800x800.png",
                    title: 'Brush',
                    price: '$15.00',
                },
                {
                    name: 'obj-2',
                    img: 'scissors-800x800.png',
                    title: 'Scissors',
                    price: '$85.00',
                },
                {
                    name: 'obj-3',
                    img: 'hot_oil_dark-800x800.png',
                    title: 'Hot Oil',
                    price: '$15.00',
                },
                {
                    name: 'obj-4',
                    img: 'straight_razor_dark-800x800.png',
                    title: 'Straight Razor',
                    price: '$30.00',
                },
            ],
            featuredCard: {
                img: 'shaving_butter-800x800.png',
                uptext: 'THIS MONTHS FEATURED PRODUCT',
                title: 'Shaving Butter',
                description: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Atque assumenda aliquid et exercitationem inventore nobis excepturi consequuntur! Esse veniam, voluptates eius magnam est ut libero.',
            },
        }
    },

    components: {
        
        mainButton,
        productsCard,
        featuredCard,

    }

}

</script>

<style lang="scss" scoped>

.bg {
    position: relative;
    width: 100%;
    background-image: url(../assets/img/avadabarbers-reviewsbackground.jpg);
    background-size: cover;
    background-position: top;
}

.container-fluid {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 990px;
    padding-bottom: 100px;
}

.row {
    width: 100%;
    padding: 0 140px;
}

.uptext {
    color: var(--primary-color);
    font-weight: 600;
}

.button {
    margin-top: var(--main-margin-y);
}

.bg:before {
    position: absolute;
    display: block;
    content: '';
    background-color: #121315;
    height: 100px;
    width: 100%;
    top: -99px;
    clip-path: polygon(50% 0%, 0% 100%, 100% 100%);
}

.featured_section {
    position: absolute;
    bottom: -415px;
    display: flex;
    justify-content: center;
    width: 100%;
    z-index: 9;
}

</style>