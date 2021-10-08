<template>
    <main>
        <!--<a-r-viewer :options="{-->
        <!--        'src': '/models/Astronaut.glb',-->
        <!--        'alt':'A 3D model of an astronaut',-->
        <!--        'ar':true,-->
        <!--        'ar-modes':'webxr scene-viewer quick-look',-->
        <!--        'environment-image': 'neutral',-->
        <!--        'auto-rotate': true,-->
        <!--        'camera-controls': true,-->
        <!--}" />-->

        <a-r-viewer
            ref="viewer"
            :options="{
                'src': '/models/dog/scene.gltf',
                'alt':'A 3D model of an astronaut',
                'ar':true,
                'ar-modes':'webxr scene-viewer quick-look',
                'environment-image': 'neutral',
                'auto-rotate': true,
                'camera-controls': true,
                'disableZoom': true,
                'arScale': '1 1 1'
        }" />

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
        --primary: teal;
        --white: #f8f8f8;
    }

    * {
        padding : 0;
        margin  : 0;
    }

    .button {
        height: 40px;

        padding: 0 16px;

        border: 0;
        outline: 0;
        background: var(--primary);
        color: var(--white);
    }

    .button.enter-ar {
        position: fixed;
        top: 0;
        left: 0;
    }
</style>
