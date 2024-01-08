<script>
export default {
    name: 'AppMain',
    data() {
        return {
            summary: [
                {
                    src: "../assets/img/buy-comics-digital-comics.png",
                    label: "DIGITAL COMICS"
                },
                {
                    src: "../assets/img/buy-comics-merchandise.png",
                    label: "DC MERCHANDISE"
                },
                {
                    src: "../assets/img/buy-comics-subscriptions.png",
                    label: "SUBSCRIPTION"
                },
                {
                    src: "../assets/img/buy-comics-shop-locator.png",
                    label: "COMIC SHOP LOCATOR"
                },
                {
                    src: "../assets/img/buy-dc-power-visa.svg",
                    label: "DC POWER VISA"
                },
            ]
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
                        <div v-for="elem, index in summary" :key="index">
                            <img :src="elem.src" :alt="elem.label">
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
    background-color: cyan;
}

#jumbo {
    background-color: black;
    padding: 30px;

    h2 {
        color: white;
    }
}
</style>