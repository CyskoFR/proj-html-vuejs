<template>
    <div class="bg">
        <div class="container">
            <div class="uptext">MENS GROOMING</div>
            <h2>Services</h2>
            <div class="row">
                <cardMain class="col" :card="card" v-for="card in cards" :key="card.name"></cardMain>
            </div>
            <mainButton class="button" :button="button"/>
        </div>
    </div>
</template>

<script>

import mainButton from '../nano-components/mainButton.vue'
import cardMain from '../micro-components/cardMain.vue'

export default {

    name: 'servicesSection',

    data() {
        return {
            button: {
                text: 'READ ABOUT OUR SERVICES',
                link: '#',
            },
            cards: [
                {
                    name: 'obj-1',
                    img: "avadabarbers-trimcut-icon-before.png",
                    title: 'Trim & Cut',
                    description: 'Avada Barbers are experts in the lickety split trim and hair cut. Quick but careful and ridiculously good looking.',
                },
                {
                    name: 'obj-2',
                    img: 'avadabarbers-washndry-icon.png',
                    title: 'Wash & Dry',
                    description: 'Take a seat in our fine leather chairs, lean back and let us lather you a fresh head in a luxurious fashion.',
                },
                {
                    name: 'obj-3',
                    img: 'avadabarbers-beardtrim-icon.png',
                    title: 'Beard Tidy',
                    description: 'Tame the tangles and untidy facial hairs like a gentleman with our Beard Tidy services from Avada Barbers.',
                },
            ]
        }
    },

    components: {
        
        mainButton,
        cardMain,

    }

}

</script>

<style lang="scss" scoped>

.bg {
    position: relative;
    width: 100%;
    background-color: white;
}

.container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: var(--main-container-width);
    min-height: 990px;
    padding-bottom: 160px;
}

.row {
    width: 100%;
    margin-bottom: var(--main-margin-y);
    margin-top: var(--main-margin-y);
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
    background-color: white;
    height: 100px;
    width: 100%;
    top: -99px;
    clip-path: polygon(50% 0%, 0% 100%, 100% 100%);
}

</style>