<template>
    <div class="bg">
        <div class="container">
            <div class="uptext">WHAT PEOPLE SAY</div>
            <h2>Reviews</h2>
            <div class="row">
                <reviewsCard class="col" :card="card" v-for="card in cards" :key="card.name"></reviewsCard>
            </div>
        </div>
    </div>
</template>

<script>

import reviewsCard from '../micro-components/reviewsCard.vue'

export default {

    name: 'reviewsSection',

    data() {
        return {
            cards: [
                {
                    name: 'obj-1',
                    img: "avadabarbers-trimcut-gallery6-200x200.jpg",
                    title: 'John Doe',
                    description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam iure consequuntur asperiores fuga impedit quia explicabo aliquid quibusdam tempore in inventore error, sunt nemo, praesentium repellendus, corrupti minima voluptates velit.',
                },
                {
                    name: 'obj-2',
                    img: 'avadabarbers-trimcut-gallery7-200x201.jpg',
                    title: 'Pete Jones',
                    description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam iure consequuntur asperiores fuga impedit quia explicabo aliquid quibusdam tempore in inventore error, sunt nemo, praesentium repellendus, corrupti minima voluptates velit.',
                },
                {
                    name: 'obj-3',
                    img: 'avadabarbers-trimcut-gallery3-200x201.jpg',
                    title: 'Mark Wilson',
                    description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam iure consequuntur asperiores fuga impedit quia explicabo aliquid quibusdam tempore in inventore error, sunt nemo, praesentium repellendus, corrupti minima voluptates velit.',
                },
            ]
        }
    },

    components: {
        
        reviewsCard,

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
    height: 1230px;
    padding-top: 540px;
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

.bg:after {
    position: absolute;
    display: block;
    content: '';
    background-color: white;
    height: 100px;
    width: 100%;
    bottom: -99px;
    clip-path: polygon(50% 0%, 0% 100%, 100% 100%);
    transform: rotate(180deg);
}

</style>