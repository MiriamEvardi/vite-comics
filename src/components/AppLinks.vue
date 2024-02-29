<script >

export default {
    name: 'AppLinks',

    data() {
        return {
            informations: [
                {
                    name: 'DIGITAL COMICS',
                    img: '/img/buy-comics-digital-comics.png'

                },
                {
                    name: 'DC MERCHANDISE',
                    img: '/img/buy-comics-merchandise.png'

                },
                {
                    name: 'SUBSCRIPTION',
                    img: '/img/buy-comics-subscriptions.png'

                },
                {
                    name: 'COMIC SHOP LOCATOR',
                    img: '/img/buy-comics-shop-locator.png'

                },
                {
                    name: 'DC POWER VISA',
                    img: '/img/buy-dc-power-visa.svg'

                },
            ]
        }
    }
}

</script>

<template>
    <div class="links-container">
        <div class="link-inner">
            <ul class="links">

                <li v-for="currentLink in informations">

                    <div class="image">
                        <img :src="currentLink.img" alt="">
                    </div>

                    <span>{{ currentLink.name }}</span>
                </li>
            </ul>

        </div>
    </div>
</template>

<style lang="scss">
@use '../src/styles/mixins' as *;
@use '../src/styles/variables' as *;

.link-inner {
    @include containerItem;
}

.links-container {
    position: relative;
    background-color: $pimaryColor;
    padding: 50px 0;
    z-index: 10;

    .links {
        @include flexItem;
        justify-content: space-between;

        color: white;
        font-weight: 400;

        li {
            @include flexItem;
            gap: 10px;
        }

        .image {
            height: 44px;

            img {
                height: 100%;
            }
        }
    }
}
</style>
