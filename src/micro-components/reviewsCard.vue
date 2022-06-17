<template>
    <div class="card">
        <p>{{card.description}}</p>
        <img :src="require('@/assets/img/' + card.img + '')" :alt="card.img">
        <h3 class="name">{{card.title}}</h3>
    </div>
</template>

<script>

export default {

    name: 'mainButton',

    props: {
        card: Object,
    }

}

</script>

<style lang="scss" scoped>

.card {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    margin: 0 42px;
    border: none;
    background: none;
}

p {
    font-size: 1.125rem;
    font-weight: 300;
    margin: 0;
}

img {
    height: 6.875rem;
    margin: 18px 0;
    border-radius: 50%;
}

h3 {
    color: var(--primary-color);
    font-weight: 600;
    font-size: 1rem;
}

</style>