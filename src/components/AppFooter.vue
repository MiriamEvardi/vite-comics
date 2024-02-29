<script>

export default {
    name: 'AppFooter',

    data() {
        return {
            social: ['/img/footer-facebook.png', '/img/footer-twitter.png', '/img/footer-youtube.png', '/img/footer-pinterest.png', '/img/footer-periscope.png']
        }
    }
}

</script>

<template>
    <div class="footer-background">
        <div class="container list">

            <div>
                <button>SIGN-UP NOW!</button>
            </div>

            <ul class="social-list">
                <li class="follow">
                    FOLLOW US
                </li>
                <li v-for="icon in social"> <img :src="icon" alt=""></li>
            </ul>


        </div>
    </div>
</template>


<style lang="scss">
@use '../styles/variables' as *;

.footer-background {
    position: relative;
    background-color: #303030;
    height: 110px;
    z-index: 10;
}

.list {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-top: 20px;
}

button {
    color: white;
    background-color: transparent;

    padding: 15px 15px;
    border: solid $pimaryColor 1px
}

.social-list {
    display: flex;
    align-items: center;

    list-style-type: none;

    gap: 20px;
}

.follow {
    color: $pimaryColor;
    font-weight: bold;
}
</style>