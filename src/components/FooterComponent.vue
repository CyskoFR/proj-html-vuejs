<template>
    <footer>
        <div class="top-section">
            <div class="container">
                <div class="row">
                    <div class="col-4 services-card">
                        <img src="../assets/img/avadabarbers_footer_shop_image-700x546.png" alt="avadabarbers_footer_shop_image-700x546.png">
                        <mainButton class="button" :button="buttonLeft" :key="buttonLeft.text"/>
                    </div>
                    <div class="col-4 info-card">
                        <img class="logo" src="../assets/img/avadabarbers-logo-x2.png" alt="avadabarbers-logo-x2.png">
                        <div class="text-area">
                            {{info.name}}<br>
                            {{info.address}}<br>
                            {{info.city}}<br>
                            {{info.email}}<br>
                            {{info.phone}}<br>
                        </div>
                        <div class="social-section">
                            <div class="social-title">FOLLOW US</div>
                            <div class="social-buttons">
                                <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
                                <a href="#"><i class="fa-brands fa-twitter"></i></a>
                                <a href="#"><i class="fa-brands fa-youtube"></i></a>
                                <a href="#"><i class="fa-brands fa-instagram"></i></a>
                            </div>
                        </div>
                    </div>
                    <div class="col-4 services-card">
                        <img src="../assets/img/avadabarbers_footer_appointment_image-700x546.png" alt="avadabarbers_footer_appointment_image-700x546.png">
                        <mainButton class="button" :button="buttonRight" :key="buttonRight.text"/>
                    </div>
                </div>
            </div>
        </div>
        <div class="bottom-section">
            <div class="container">&#169; Copyright 2012 - 2020 | Avada Theme by ThemeFusion | All Rights Reserved | Powered by Cysko</div>
        </div>
    </footer>
</template>

<script>

import mainButton from '../nano-components/mainButton.vue'

export default {

    name: 'FooterComponent',

    data() {

        return {

            buttonLeft: {
                text: 'SHOP OUR RANGE NOW',
                link: '#',
            },

            buttonRight: {
                text: 'BOOK YOUR APPOINTMENT',
                link: '#',
            },

            info: {
                name: 'Avada Barbers',
                address: '123 New York Street',
                city: 'New York City',
                email: 'info@yourwebsite.com',
                phone: '+1 (555) 555-1212',
            }

        }

    },

    components: {
        
        mainButton,

    },

}

</script>

<style lang="scss" scoped>

.top-section {
    background-color: #121314;
    padding: 55px 0;
    .row {
        padding: 0 50px;
    }
    img {
        max-height: 240px;
        margin-bottom: 30px;
    }
    .logo {
        max-width: 180px;
        margin-bottom: 0;
    }
}

.services-card {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.info-card {
    display: flex;
    flex-direction: column;
    align-items: center;
    .logo {
        max-width: 175px;
    }
    .text-area {
        text-align: center;
        color: grey;
        font-size: .875rem;
        margin: 50px 0;
    }
    .social-section {
        .social-title {
            display: flex;
            justify-content: center;
            color: var(--primary-color);
            font-weight: 600;
            margin-bottom: 30px;
        }
        .social-buttons {
            display: flex;
            justify-content: center;
            gap: 14px;
            a {
                color: var(--secondary-color);
            }
        }
    }
}

.bottom-section {
    text-align: center;
    background-color: #161718;
    padding: 36px 0;
    color: grey;
    margin: none;
    font-size: .75rem;
}

</style>