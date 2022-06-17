<template>
    <div class="bg">
        <div class="container">
            <div class="uptext">TALES FROM THE BARBER SHOP</div>
            <h2>Recent Blog Posts</h2>
            <div class="row">
                <blogCard class="col" :card="card" v-for="card in cards" :key="card.name"></blogCard>
            </div>
            <mainButton class="button" :button="button"/>
        </div>
    </div>
</template>

<script>

import mainButton from '../nano-components/mainButton.vue'
import blogCard from '../micro-components/blogCard.vue'

export default {

    name: 'recentBlogSection',

    data() {
        return {
            button: {
                text: 'READ MORE FROM OUR BLOG',
                link: '#',
            },
            cards: [
                {
                    name: 'obj-1',
                    img: "avadabarbers-second-blog-700x441.jpg",
                    title: 'Avada Barbers Now Open',
                    description: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Atque assumenda aliquid et exercitationem inventore.',
                },
                {
                    name: 'obj-2',
                    img: 'avadabarbers-choosing-blog-700x441.jpg',
                    title: 'Choosing The Right Barber',
                    description: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Atque assumenda aliquid et exercitationem inventore.',
                },
                {
                    name: 'obj-3',
                    img: 'avadabarbers-ourservice-blog-700x441.jpg',
                    title: 'Quick Service Guide',
                    description: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Atque assumenda aliquid et exercitationem inventore.',
                },
            ]
        }
    },

    components: {
        
        mainButton,
        blogCard,

    }

}

</script>

<style lang="scss" scoped>

.bg {
    width: 100%;
    background-color: #f5f5f5;
}

.container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: var(--main-container-width);
    height: 1080px;
}

.row {
    width: 100%;
    margin: 18px 0;
}

.col {
    margin: 0 15px;
    padding: 0;
}

.uptext {
    color: var(--primary-color);
    font-weight: 600;
}

.button {
    margin-top: var(--main-margin-y);
}


</style>