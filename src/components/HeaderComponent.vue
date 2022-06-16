<template>
    <header>
        <div class="header_container container py-3">
            <img class="header_logo" src="../assets/img/avadabarbers-logo-x1.png" alt="avadabarbers-logo-x1.png">
            <nav class="header_nav">
                <ul>
                    <li><i class="fa-solid fa-cart-shopping"></i></li>
                    <li><i class="fa-solid fa-bars"></i></li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<script>
export default {

    name: 'HeaderComponent',

}
</script>

<style lang="scss" scoped>

header {
    position: absolute;
    width: 100%;
}

.header_container {
    display: flex;
    align-items: center;
    justify-content: space-between;
    max-width: var(--main-container-width);
    height: 100px;
    .header_logo {
        width: 11.875rem;
    }
}
.header_nav ul {
    display: flex;
    margin: 0;
    li {
        list-style: none;
        color: white;
        margin: 0 12px;
        font-size: 20px;
    }
}

</style>