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

        <a-r-viewer :options="{
                'src': '/models/dog/scene.gltf',
                'alt':'A 3D model of an astronaut',
                'ar':true,
                'ar-modes':'webxr scene-viewer quick-look',
                'environment-image': 'neutral',
                'auto-rotate': true,
                'camera-controls': true,
        }" />

    </main>
</template>

<script>
    import ARViewer from '../components/AR-viewer';

    export default {
        components: { ARViewer },
    };
</script>

<style>
    * {
        padding : 0;
        margin  : 0;
    }
</style>
