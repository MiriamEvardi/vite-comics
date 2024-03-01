<script>

export default {
    name: 'ComicsItem',

    props: {
        comicsImage: String,
        comicsTitle: String,
    }
}

</script>

<template>
    <div class="comic">
        <img :src="comicsImage" :alt="comicsTitle">
        <div> {{ comicsTitle }}</div>

    </div>
</template>


<style lang="scss">
@use '../styles/general.scss' as *;

.comic {
    width: calc(100% / 6);
    height: 195px;
    padding: 15px;
    margin-bottom: 30px;

    img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: top;
    }

    div {
        margin-top: 10px;
        text-transform: uppercase;
        line-height: 1.2em;
        font-size: 0.8em;
    }
}
</style>