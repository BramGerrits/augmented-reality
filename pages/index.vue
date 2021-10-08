<template>
    <main>
        <nav class="nav">
            <div class="logo">
                Wannabe Floor Company
            </div>
        </nav>
        <section class="product-grid">
            <div class="product">
                <div class="model">
                    <a-r-viewer
                        ref="floorViewer"
                        :scale="0.40"
                        :options="{
                            'src': '/models/floor/floertje.glb',
                            'alt':'A 3D model of an astronaut',
                            'ar-placement': 'floor'
                        }"
                    />
                </div>

                <div class="title-wrapper">
                    <h2>Vloertje</h2>
                    <button class="enter-ar-btn" @click="$refs.floorViewer.enterAR()">
                        <svg width="25" height="25" viewBox="0 0 25 25" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M17.687 22.5197V20.5197H20.687V17.5197H22.687V21.0197C22.687 21.4097 22.527 21.7597 22.227 22.0597C21.927 22.3597 21.577 22.5197 21.187 22.5197H17.687ZM7.68701 22.5197H4.18701C3.79701 22.5197 3.44701 22.3597 3.14701 22.0597C2.84701 21.7597 2.68701 21.4097 2.68701 21.0197V17.5197H4.68701V20.5197H7.68701V22.5197ZM17.687 2.51965H21.187C21.577 2.51965 21.927 2.67965 22.227 2.97965C22.527 3.27965 22.687 3.62965 22.687 4.01965V7.51965H20.687V4.51965H17.687V2.51965ZM7.68701 2.51965V4.51965H4.68701V7.51965H2.68701V4.01965C2.68701 3.62965 2.84701 3.27965 3.14701 2.97965C3.44701 2.67965 3.79701 2.51965 4.18701 2.51965H7.68701ZM13.687 17.7697L17.687 15.4697V10.8797L13.687 13.1797V17.7697ZM12.687 11.4397L16.687 9.14965L12.687 6.79965L8.68701 9.14965L12.687 11.4397ZM7.68701 15.4697L11.687 17.7697V13.1797L7.68701 10.8797V15.4697ZM18.917 8.10965C19.417 8.42965 19.687 8.85965 19.687 9.42965V15.7497C19.687 16.3197 19.417 16.7497 18.917 17.0697L13.437 20.2497C12.937 20.5697 12.437 20.5697 11.937 20.2497L6.45701 17.0697C5.95701 16.7497 5.68701 16.3197 5.68701 15.7497V9.42965C5.68701 8.85965 5.95701 8.42965 6.45701 8.10965L11.937 4.92965C12.187 4.79965 12.437 4.73965 12.687 4.73965C12.937 4.73965 13.187 4.79965 13.437 4.92965L18.917 8.10965Z"
                                  fill="black" />
                        </svg>
                    </button>
                </div>
            </div>

            <div class="product">
                <div class="model">
                    <a-r-viewer
                        ref="viewer"
                        :scale="0.45"
                        :options="{
                            'src': '/models/model/testdonut.glb',
                            'alt':'A 3D model of an astronaut',
                            'ar-placement': 'wall'
                        }"
                    />
                </div>

                <div class="title-wrapper">
                    <h2>Muurtje</h2>
                    <button class="enter-ar-btn" @click="$refs.viewer.enterAR()">
                        <svg width="25" height="25" viewBox="0 0 25 25" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M17.687 22.5197V20.5197H20.687V17.5197H22.687V21.0197C22.687 21.4097 22.527 21.7597 22.227 22.0597C21.927 22.3597 21.577 22.5197 21.187 22.5197H17.687ZM7.68701 22.5197H4.18701C3.79701 22.5197 3.44701 22.3597 3.14701 22.0597C2.84701 21.7597 2.68701 21.4097 2.68701 21.0197V17.5197H4.68701V20.5197H7.68701V22.5197ZM17.687 2.51965H21.187C21.577 2.51965 21.927 2.67965 22.227 2.97965C22.527 3.27965 22.687 3.62965 22.687 4.01965V7.51965H20.687V4.51965H17.687V2.51965ZM7.68701 2.51965V4.51965H4.68701V7.51965H2.68701V4.01965C2.68701 3.62965 2.84701 3.27965 3.14701 2.97965C3.44701 2.67965 3.79701 2.51965 4.18701 2.51965H7.68701ZM13.687 17.7697L17.687 15.4697V10.8797L13.687 13.1797V17.7697ZM12.687 11.4397L16.687 9.14965L12.687 6.79965L8.68701 9.14965L12.687 11.4397ZM7.68701 15.4697L11.687 17.7697V13.1797L7.68701 10.8797V15.4697ZM18.917 8.10965C19.417 8.42965 19.687 8.85965 19.687 9.42965V15.7497C19.687 16.3197 19.417 16.7497 18.917 17.0697L13.437 20.2497C12.937 20.5697 12.437 20.5697 11.937 20.2497L6.45701 17.0697C5.95701 16.7497 5.68701 16.3197 5.68701 15.7497V9.42965C5.68701 8.85965 5.95701 8.42965 6.45701 8.10965L11.937 4.92965C12.187 4.79965 12.437 4.73965 12.687 4.73965C12.937 4.73965 13.187 4.79965 13.437 4.92965L18.917 8.10965Z"
                                  fill="black" />
                        </svg>
                    </button>
                </div>
            </div>
        </section>
    </main>
</template>

<script>
    import ARViewer from '../components/AR-viewer';

    export default {
        components: { ARViewer },
    };
</script>

<style>
    @import url('https://fonts.googleapis.com/css?family=Poppins&display=swap');

    :root {
        --primary : #F5CB5C;
        --white   : #F8F8F8;
        --black   : #151515;
        --gray    : rgb(240, 240, 240);

        --outer   : 240px;
    }

    @media (max-width : 572px) {
        :root {
            --outer : 24px;
        }
    }

    * {
        font-family : Poppins;
        padding     : 0;
        margin      : 0;
        box-sizing  : border-box;
        color       : var(--black);
    }

    main {
        width      : 100%;
        min-height : 100vh;
        background : var(--white);
    }

    button {
        border  : 0;
        outline : 0;
    }

    svg path {
        fill : var(--black);
    }

    .nav {
        position      : fixed;
        top           : 0;
        left          : 0;
        height        : 80px;
        /*width         : 100%;*/

        display       : flex;
        align-items   : center;

        padding-left  : var(--outer);
        padding-right : var(--outer)
    }

    .nav .logo {
        font-family : 'Comic Sans MS';
    }

    .product-grid {
        padding-left   : var(--outer);
        padding-right  : var(--outer);
        padding-top     : 120px;
        display        : grid;
        gap            : 24px;
        grid-auto-flow : row;
        grid-auto-rows : max-content;
        width          : 100%;
    }

    .product-grid .product {
        background : var(--gray);
        padding    : 24px;
    }

    .product-grid .product .model {
        height        : 200px;
        margin-bottom : 16px;
        width         : 100%;
    }

    .product-grid .product .title-wrapper {
        display         : flex;
        align-items     : center;
        justify-content : space-between;
    }

    .button {
        height     : 40px;

        padding    : 0 16px;

        border     : 0;
        outline    : 0;
        background : var(--primary);
        color      : var(--white);
    }

    .button.enter-ar {
        position : fixed;
        top      : 0;
        left     : 0;
    }

    .enter-ar-btn {
        display         : flex;
        align-items     : center;
        justify-content : center;
        height          : 48px;
        width           : 48px;
        border-radius   : 48px;

        box-shadow      : 0 0 16px rgba(0, 0, 0, 0.1);
        background      : var(--primary);
    }
</style>
