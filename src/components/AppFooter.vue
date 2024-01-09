<script>
export default {
    name: 'AppFooter',
    data() {
        return {
            dc_comics: ['Characters', 'Comics', 'Movies', 'TV', 'Games', 'Videos', 'News'],
            dc: ['Terms Of Use', 'Privacy policy (New)', 'Ad Choices', 'Adversiting', 'Jobs', 'Subscriptions', 'Talent Workshops', 'CPSC Certificates', 'Ratings', 'Shop Help', 'Contact Us'],
            sites: ['DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa'],
            shop: ['Shop DC', 'Shop DC Collectibles'],
            summary: [
                {
                    img: "buy-comics-digital-comics.png",
                    label: "DIGITAL COMICS"
                },
                {
                    img: "buy-comics-merchandise.png",
                    label: "DC MERCHANDISE"
                },
                {
                    img: "buy-comics-subscriptions.png",
                    label: "SUBSCRIPTION"
                },
                {
                    img: "buy-comics-shop-locator.png",
                    label: "COMIC SHOP LOCATOR"
                },
                {
                    img: "buy-dc-power-visa.svg",
                    label: "DC POWER VISA"
                },
            ]
        }
    },
    methods: {
        getImagePath: function (imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    },
}
</script>
<template lang="">
    <footer>

        <section id="summary">
            <div class="container">
                <div class="row">
                    <div class="col-12 d-flex gap-1">
                        <div v-for="elem, index in summary" :key="index" class="d-flex p-4 gap-2 align-items-center justify-content-center">
                            <img :src="getImagePath(`../assets/img/${elem.img}`)" :alt="elem.label" class="img-fluid">
                            <p>{{elem.label}}</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="lists">
            <div class="container">
                <div class="row">
                    <div class="col-6 d-flex flex-wrap gap-5 p-5">
                        <div>
                            <h2>DC COMICS</h2>
                            <ul class="list-unstyled">
                                <li v-for="comics, index in dc_comics" :key="index"><a href="#">{{comics}}</a></li>
                            </ul>
                            <div>
                                <h2>SHOP</h2>
                                <ul class="list-unstyled">
                                    <li v-for="shop, index in shop" :key="index"><a href="#">{{shop}}</a></li>
                                </ul>
                            </div>
                        </div>
                        <div>
                            <h2>DC</h2>
                            <ul class="list-unstyled">
                                <li v-for="dc, index in dc" :key="index"><a href="#">{{dc}}</a></li>
                            </ul>
                        </div>
                        <div>
                            <h2>SITES</h2>
                            <ul class="list-unstyled">
                                <li v-for="sites, index in sites" :key="index"><a href="#">{{sites}}</a></li>
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
                    <div class="col-12 d-flex justify-content-between align-items-center">
                        <button class="text-uppercase">sign up now!</button>
                        <div class="socials d-flex align-items-center gap-4">
                            <h4>FOLLOW US</h4>
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

#summary {
    background-color: #0082F9;
    color: #fff;

    img {
        width: 27%;
    }
}

#lists {
    background-image: url(../assets/img/footer-bg.jpg);
    background-size: cover;

    h2 {
        color: #fff;
        font-weight: bolder;
    }

    li a {
        color: #959696;
        text-decoration: none;
    }

    .bglogo {
        background-image: url(../assets/img/dc-logo-bg.png);
        background-repeat: no-repeat;
        background-position: center;
        background-size: cover;
    }
}

#links {
    background-color: #303030;
    padding: 20px;

    h4 {
        color: #0083F8;
        font-weight: bolder;
    }

    button {
        background-color: transparent;
        border: 2px solid #0082F9;
        padding: 15px;
        color: #fff;
        transition: background-color 0.4s;

        &:hover {
            background-color: #0082F9;
        }
    }
}
</style>