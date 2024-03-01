<script >
export default {
    name: 'AppNav',

    data() {
        return {
            links: ['CHARACTERS', 'COMICS', 'MOVIES', 'TV', 'GAMES', 'COLLECTIBLES', 'VIDEOS', 'FANS', 'NEWS', 'SHOP'],

            activeIndex: 0,
        }
    },

    methods: {
        activeLink(index) {
            this.activeIndex = index;
        }
    }
}

</script>

<template>
    <nav>


        <div class="container">

            <img id="logo" src="/img/dc-logo.png" alt="">


            <ul class="links">
                <li v-for="(currentLink, index) in links" :class="index == activeIndex ? 'active' : ''"
                    @click="activeLink(index)">
                    {{ currentLink }}</li>
            </ul>
        </div>

    </nav>
</template>


<style lang="scss">
@use '../src/styles/mixins' as *;
@use '../src/styles/variables' as *;

nav {
    background-color: aliceblue;

    height: 120px;

    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;

        height: 100%;
    }

    #logo {
        height: 80px;
    }


}

ul.links {
    @include flexItem;
    align-items: stretch;
    gap: 30px;

    height: 100%;

    margin: 0;

    list-style-type: none;

    color: #464646;
    font-weight: bold;

    li {
        position: relative;

        display: flex;
        align-items: center;

        &.active::before {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;

            width: 100%;
            height: 6px;

            background-color: $primaryColor;

        }

        &.active {
            color: $primaryColor;
        }
    }
}
</style>
