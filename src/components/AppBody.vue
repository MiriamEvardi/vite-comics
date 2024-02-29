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
                    comics: ['Characters', 'Comics', '']
                }
            ],

        }
    },
}

</script>

<template>
    <AppLinks></AppLinks>

    <div>
        <div class="container ">
            <div>
                <h2>a</h2>
                <ul>
                    <li></li>
                </ul>

                <h2></h2>
                <ul>
                    <li></li>
                </ul>
            </div>
            <div>
                <h2></h2>
                <ul>
                    <li></li>
                </ul>
            </div>
            <div>
                <h2></h2>
                <ul>
                    <li></li>
                </ul>
            </div>
        </div>

        <div>

        </div>


    </div>
</template>

<style lang="scss">
@use '../src/styles/mixins' as *;
@use '../src/styles/variables' as *;
</style>
