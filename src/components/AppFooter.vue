<script>
export default {
    name: 'AppFooter',
    data() {
        return {
            dc_comics: ['Characters', 'Comics', 'Movies', 'TV', 'Games', 'Videos', 'News'],
            dc: ['Terms Of Use', 'Privacy policy (New)', 'Ad Choices', 'Adversiting', 'Jobs', 'Subscriptions', 'Talent Workshops', 'CPSC Certificates', 'Ratings', 'Shop Help', 'Contact Us'],
            sites: ['DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa'],
            shop: ['Shop DC', 'Shop DC Collectibles']
        }
    },
}
</script>
<template lang="">
    <footer>
        <section id="lists">
            <div class="container">
                <div class="row">
                    <div class="col-6 d-flex flex-wrap gap-5 p-5">
                        <div>
                            <h2>DC COMICS</h2>
                            <ul class="list-unstyled">
                                <li v-for="comics, index in dc_comics" :key="index">{{comics}}</li>
                            </ul>
                            <div>
                                <h2>SHOP</h2>
                                <ul class="list-unstyled">
                                    <li v-for="shop, index in shop" :key="index">{{shop}}</li>
                                </ul>
                            </div>
                        </div>
                        <div>
                            <h2>DC</h2>
                            <ul class="list-unstyled">
                                <li v-for="dc, index in dc" :key="index">{{dc}}</li>
                            </ul>
                        </div>
                        <div>
                            <h2>SITES</h2>
                            <ul class="list-unstyled">
                                <li v-for="sites, index in sites" :key="index">{{sites}}</li>
                            </ul>
                        </div>
                    </div>
                    <div class="col-6 bglogo">
                    </div>
                </div>
            </div>
        </section>
        <section id="links">
            <div class="container">
                <div class="row">
                    <div class="col-12 d-flex justify-content-between">
                        <button class="btn btn-outline-primary text-uppercase">sign up now</button>
                        <div class="socials d-flex align-items-center gap-2">
                            <h2>FOLLOW US</h2>
                            <img src="../assets/img/footer-facebook.png" alt="facebook">
                            <img src="../assets/img/footer-twitter.png" alt="twitter">
                            <img src="../assets/img/footer-youtube.png" alt="youtube">
                            <img src="../assets/img/footer-pinterest.png" alt="pinterest">
                            <img src="../assets/img/footer-periscope.png" alt="periscope">
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </footer>
</template>
<style lang="scss" scoped>
@use '../styles/generals.scss';

#lists {
    background-image: url(../assets/img/footer-bg.jpg);
    background-size: cover;

    h2 {
        color: #fff;
        font-weight: bolder;
    }

    li {
        color: #959696;
    }

    .bglogo {
        background-image: url(../assets/img/dc-logo-bg.png);
        background-repeat: no-repeat;
        background-size: cover;
    }
}

#links {
    background-color: #303030;
    padding: 20px;

    h2 {
        color: #0083F8;
        font-weight: bolder;
    }
}
</style>