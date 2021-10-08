<template>
    <main>
        <a-r-viewer
            ref="viewer"
            :scale="0.45"
            :options="{
                'src': '/models/model/testdonut.glb',
                'alt':'A 3D model of an astronaut',
                'ar-placement': 'floor'
            }"
        />

        <button class="button enter-ar" @click="$refs.viewer.enterAR()">
            hatseflats
        </button>
    </main>
</template>

<script>
    import ARViewer from '../components/AR-viewer';

    export default {
        components: { ARViewer },
    };
</script>

<style>
    :root {
        --primary : teal;
        --white   : #F8F8F8;
    }

    * {
        padding : 0;
        margin  : 0;
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
</style>
