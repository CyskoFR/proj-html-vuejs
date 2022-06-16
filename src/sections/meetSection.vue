<template>
    <div class="bg">
        <div class="container">
            <div class="uptext">AWARD WINNING</div>
            <h2>Pro Barbers</h2>
            <mainButton :button="meetButton"/>
        </div>
    </div>
</template>

<script>

import mainButton from '../nano-components/mainButton.vue'

export default {

    name: 'meetSection',

    data() {
        return {
            meetButton: {
                text: 'MEET YOUR NEW BARBEER',
                link: '#',
            }
        }
    },

    components: {
        
        mainButton,

    }

}

</script>

<style lang="scss" scoped>

.bg {
    width: 100%;
    background-image: url(../assets/img/avadabarbers-about-introbackground.jpg);
    background-position: top;
    background-size: cover;
}

.container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: var(--main-container-width);
    height: 555px;
}

.uptext {
    color: var(--primary-color);
    font-weight: 600;
}

</style>