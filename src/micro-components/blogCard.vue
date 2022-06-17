<template>
    <div class="blogCard">
        <img :src="require('@/assets/img/' + card.img + '')" :alt="card.img">
        <div class="text-area">
            <h3>{{card.title}}</h3>
            <p>{{card.description}}</p>
        </div>
    </div>
</template>

<script>

export default {

    name: 'blogCard',

    props: {
        card: Object,
    }

}

</script>

<style lang="scss" scoped>

.blogCard {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    margin: 0 42px;
    border: none;
    background: none;
}

img {
    width: 100%;
    margin-bottom: 20px;
}

.text-area {
    padding: 0 16px;
}

h3 {
    color: var(--primary-color);
    margin-bottom: 14px;
}

p {
    font-size: 1.125rem;
}

</style>