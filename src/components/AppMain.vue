<script>
export default {
    name: 'AppMain',
    data() {
        return {

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
                        <div>
                            <img src="../assets/img/buy-comics-digital-comics.png" alt="digital">
                            <p>DIGITAL COMICS</p>
                        </div>
                        <div>
                            <img src="../assets/img/buy-comics-merchandise.png" alt="merch">
                            <p>DC MERCHANDISE</p>
                        </div>
                        <div>
                            <img src="../assets/img/buy-comics-subscriptions.png" alt="sub">
                            <p>SUBSCRIPTION</p>
                        </div>
                        <div>
                            <img src="../assets/img/buy-comics-shop-locator.png" alt="shop">
                            <p>COMIC SHOP LOCATOR</p>
                        </div>
                        <div>
                            <img src="../assets/img/buy-dc-power-visa.svg" alt="visa">
                            <p>DC POWER VISA</p>
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