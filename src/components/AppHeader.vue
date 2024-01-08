<script>
export default {
    name: 'AppHeader',
    data() {
        return {

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
                            <li>Characters</li>
                            <li>Comics</li>
                            <li>Movies</li>
                            <li>Tv</li>
                            <li>Games</li>
                            <li>Collectibles</li>
                            <li>Videos</li>
                            <li>Fans</li>
                            <li>News</li>
                            <li>Shop</li>
                        </ul>
                    </nav>
                </div>
            </div>
        </div>
    </header>
</template>
<style lang="scss" scoped>
@use '../styles/generals.scss';
</style>