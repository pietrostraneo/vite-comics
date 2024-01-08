<script>
export default {
    name: 'AppMain',
    data() {
        return {
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
    <main>

        <section id="jumbo">
            <div class="container">
                <div class="row">
                    <div class="col-12">
                        <div>
                            <h2>content goes here</h2>
                        </div>
                    </div>
                </div>
            </div>
        </section>

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

    </main>
</template>
<style lang="scss" scoped>
@use '../styles/generals.scss';

main {
    margin-top: 15px;
}

#summary {
    background-color: #0082F9;
    color: #fff;

    img {
        width: 27%;
    }
}

#jumbo {
    background-color: black;
    padding: 50px;

    h2 {
        color: white;
    }
}
</style>