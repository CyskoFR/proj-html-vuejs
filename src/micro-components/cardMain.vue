<template>
    <div class="card">
        <img :src="require('@/assets/img/' + card.img + '')" :alt="card.img">
        <h3>{{card.title}}</h3>
        <p>{{card.description}}</p>
    </div>
</template>

<script>

export default {

    name: 'cardMain',

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

img {
    height: 6.875rem;
    margin-bottom: var(--main-margin-y);
    margin-top: var(--main-margin-y);
}

h3 {
    color: var(--primary-color);
}

p {
    font-size: 1.125rem;
}

</style>