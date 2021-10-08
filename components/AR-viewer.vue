<template>
    <div
        class="container"
        :class="{
            'no-button' : hideButton
        }"
        ref="container"/>
</template>

<script>
    export default {
        name: 'AR-viewer',

        props: {
            options: {
                type: Object,
                default: () => ({})
            },
            hideButton: {
                type: Boolean,
                default: () => false
            },
            scale: {
                type: Number,
                default: () => 1
            }
        },

        async mounted() {
            if (process.browser) {
                const options = this.options;
                const scale = this.scale;
                const parent = this.$refs['container'];

                const Module = await import('@google/model-viewer');
                const element = new Module.ModelViewerElement();

                element.onload = (event) => {
                    // console.log(event)
                }

                Object.entries(options).forEach((entry) => {
                    const name = entry[0]
                    const value = entry[1]

                    element[name] = value
                })

                element.scale = `${scale} ${scale} ${scale}`

                parent.appendChild(element)
            }
        },

        methods: {
            enterAR() {
                const viewer = this.$refs.container.children[0]
                viewer.activateAR()
            },
        }
    };
</script>

<style scoped>
    .container {
        height: 100vh;
        width: 100vw;
    }

    /*.container.no-button::v-deep #default-ar-button {*/
    /*    display: none;*/
    /*    background: red;*/
    /*}*/

    .container::v-deep > * {
        height: 100%;
        width: 100%;
    }
</style>
