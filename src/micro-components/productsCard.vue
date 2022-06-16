<template>
    <div class="card">
        <img :src="require('@/assets/img/' + card.img + '')" :alt="card.img">
        <h3>{{card.title}}</h3>
        <p>{{card.price}}</p>
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
    margin: 0 30px;
    border: none;
    background: none;
}

img {
    height: 21.25rem;
    margin-bottom: var(--main-margin-y);
    margin-top: var(--main-margin-y);
}

h3 {
    color: var(--primary-color);
    margin-bottom: 1rem;
}

p {
    font-size: 1.125rem;
    font-weight: 200;
    color: var(--primary-color);
}

</style>