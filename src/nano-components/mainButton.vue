<template>
    <div class="main_button">{{button.text}}</div>
</template>

<script>
export default {

    name: 'mainButton',

    props: {
        button: Object,
    }

}
</script>

<style lang="scss" scoped>

.main_button {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    border: 2px solid var(--primary-color);
    color: var(--primary-color);
    width: fit-content;
    padding: 12px 36px;
    font-size: .875rem;
    font-weight: 600;
    cursor: pointer;
}

.main_button:hover {
    transform: scale(105%);
    background-color: darken($color: #1d1d1d, $amount: 0);
}

</style>