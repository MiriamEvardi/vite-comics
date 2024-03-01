<script >
import AppLinks from './AppLinks.vue';

export default {
    components: {
        AppLinks,
    },

    name: 'AppBody',


    data() {
        return {
            linkList: [
                {
                    title: 'DC COMICS',
                    items: ['Characters', 'Comics', 'Movies', 'TV', 'Games', 'Videos', 'News']
                },
                {
                    title: 'SHOP',
                    items: ['Shop DC', 'Shop DC Collectibles']
                },
                {
                    title: 'DC',
                    items: ['Term Of Use', 'Privacy policy (New)', 'Advertising', 'Jobs', 'Subscriptions', 'Talent Workshops', 'CPSC Certificates', 'Ratings', 'Shop Help', 'Contact Us']
                },
                {
                    title: 'SITES',
                    items: ['DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa']
                }
            ],

        }
    },
}

</script>

<template>
    <div>
        <AppLinks></AppLinks>

        <div class="background">
            <div class="container">

                <div class="link-list">

                    <div v-for="currentLinkList in linkList">
                        <h4>{{ currentLinkList.title }}</h4>
                        <ul>
                            <li v-for="currentLink in currentLinkList.items">{{ currentLink }}</li>

                        </ul>
                    </div>

                </div>

                <div class="big-logo">
                    <img src="/img/dc-logo-bg.png" alt="">
                </div>

            </div>
        </div>
    </div>
</template>

<style lang="scss">
@use '../src/styles/mixins' as *;
@use '../src/styles/variables' as *;
@use '../styles/general' as *;


.background {
    height: 370px;

    background-image: url('/img/footer-bg.jpg');
    background-position: cover;

    overflow: hidden;

    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;

        height: 100%;


    }




    ul {
        list-style-type: none;
        padding: 0;

        color: #ccc;
        font-size: .9 em;
    }

    .link-list {
        display: flex;
        flex-flow: column wrap;
        align-content: flex-start;
        gap: 10px 30px;

        height: 100%;

        padding: 20px 0;


        h4 {
            font-size: 1.5em;

            margin-bottom: 10px;
        }
    }


}
</style>
