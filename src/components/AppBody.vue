<script >
import AppLinks from './AppLinks.vue';

export default {
    components: {
        AppLinks,
    },

    name: 'AppBody',


    data() {
        return {
            links: [
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
    <div class="background">
        <AppLinks></AppLinks>

        <div class="container">
            <div class="big-logo"><img src="/img/dc-logo-bg.png" alt=""></div>
            <div class="column">
                <h2>{{ links[0].title }}</h2>
                <ul class="bottom-links">
                    <li class="column-list" v-for="(item, index) in links[0].items" :key="index">{{ item }}</li>
                </ul>
                <h2>{{ links[1].title }}</h2>
                <ul class="bottom-links">
                    <li class="column-list" v-for="(item, index) in links[1].items" :key="index">{{ item }}</li>
                </ul>
            </div>
            <div class="column">
                <h2>{{ links[2].title }}</h2>
                <ul class="bottom-links">
                    <li class="column-list" v-for="(item, index) in links[2].items" :key="index">{{ item }}</li>
                </ul>
            </div>
            <div class="column">
                <h2>{{ links[3].title }}</h2>
                <ul class="bottom-links">
                    <li class="column-list" v-for="(item, index) in links[3].items" :key="index">{{ item }}</li>
                </ul>
            </div>




        </div>
    </div>
</template>

<style lang="scss">
@use '../src/styles/mixins' as *;
@use '../src/styles/variables' as *;


.background {
    position: relative;
    background-image: url(/img/footer-bg.jpg);
    background-size: cover;


}

.container {
    @include containerItem;

    display: flex;
    align-items: flex-start;
    gap: 50px;

    .column {
        flex-direction: column;
        align-items: start;

        h2 {
            margin-bottom: 0;
        }
    }

    .bottom-links {
        list-style-type: none;
        padding: 0;

        .column-list {
            display: flex;
            justify-content: flex-start;
        }
    }
}


.big-logo {
    position: absolute;
    right: 15%;
    bottom: -10%;
}
</style>
