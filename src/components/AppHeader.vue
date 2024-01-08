<script>
export default {
    name: 'AppHeader',
    data() {
        return {
            menu: [
                {
                    label: "Characters",
                    active: false
                },
                {
                    label: "Comics",
                    active: true
                },
                {
                    label: "Movies",
                    active: false
                },
                {
                    label: "TV",
                    active: false
                },
                {
                    label: "Games",
                    active: false
                },
                {
                    label: "Collectibles",
                    active: false
                },
                {
                    label: "Videos",
                    active: false
                },
                {
                    label: "Fans",
                    active: false
                },
                {
                    label: "News",
                    active: false
                },
                {
                    label: "Shop",
                    active: false
                },
            ]
        }
    },
}
</script>
<template lang="">
    <header>
        <div class="container">
            <div class="row">
                <div class="col-12">
                    <nav class="d-flex justify-content-between align-items-center mt-3">
                        <img src="../assets/img/dc-logo.png" alt="logo">
                        <ul class="d-flex gap-3 list-unstyled text-uppercase">
                            <li v-for="nav, index in menu" :key="index">
                                <a href="#" :class="nav.active ? 'active' : ''">{{nav.label}}</a>
                            </li>
                        </ul>
                    </nav>
                </div>
            </div>
        </div>
    </header>
</template>
<style lang="scss" scoped>
@use '../styles/generals.scss';

a {
    text-decoration: none;
    color: black;
    font-weight: 300;
}

.active {
    color: #0083F8;
    border-bottom: 3px solid #0083F8;
}
</style>