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

            <div>
                <div>
                    <img src="/img/dc-logo.png" alt="">
                </div>

                <ul id="links">
                    <li v-for="(currentLink, index) in links" :class="index == activeIndex ? 'active' : ''"
                        @click="activeLink(index)">
                        {{ currentLink }}</li>
                </ul>
            </div>

        </div>
    </nav>
</template>


<style lang="scss">
$pimaryColor: #0282f9;

@mixin flexItem {
    display: flex;
    align-items: center;
}

nav {
    background-color: aliceblue;

    height: 120px;

    padding-top: 20px;
}

.container {

    width: 80vw;
    max-width: 1200px;
    padding: 0 200px;

    margin: 0 auto;

    div {
        @include flexItem;
        justify-content: space-between;
    }
}

#links {
    @include flexItem;

    list-style-type: none;

    color: #464646;
    font-weight: bold;

    gap: 30px;

    .active {
        border-bottom: $pimaryColor solid 4px;
    }
}
</style>
