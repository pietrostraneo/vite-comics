<script>
export default {
    name: 'AppComic',
    props: {
        img: String,
        title: String
    },
    data() {
        return {

        }
    },
}
</script>
<template lang="">
    <div class="col-2">
        <div class="thumbnails">
            <img :src="img" :alt="title" class="img-fluid">
            <p class="text-uppercase">{{title}}</p>
        </div>
    </div>
</template>
<style lang="scss" scoped>
@use '../styles/generals.scss';

.thumbnails {
    margin: 28px 0;

    img {
        width: 250px;
        height: 200px;
    }

    p {
        color: white;
        font-weight: bold;
        margin-top: 5px;
    }
}
</style>