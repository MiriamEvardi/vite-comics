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
        <div class="nav-container">

            <div class="inner-container">
                <div>
                    <img src="/img/dc-logo.png" alt="">
                </div>

                <ul class="links">
                    <li v-for="(currentLink, index) in links" :class="index == activeIndex ? 'active' : ''"
                        @click="activeLink(index)">
                        {{ currentLink }}</li>
                </ul>
            </div>

        </div>
    </nav>
</template>


<style lang="scss">
@use '../src/styles/mixins' as *;
@use '../src/styles/variables' as *;
@use '../styles/mixins' as *;


nav {
    background-color: aliceblue;
    width: 100%;

    height: 120px;

    padding-top: 20px;

    .nav-container {
        @include containerItem;

    }
}


.inner-container {
    display: flex;
    justify-content: space-between;
}



.links {
    @include flexItem;

    list-style-type: none;

    color: #464646;
    font-weight: bold;

    gap: 30px;

    .active {
        border-bottom: $pimaryColor solid 4px;

        color: $pimaryColor;
    }
}
</style>
