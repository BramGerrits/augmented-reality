<template>
    <div class="container" ref="container"/>
</template>

<script>
    export default {
        name: 'AR-viewer',

        props: {
            options: {
                type: Object,
                default: () => ({})
            }
        },

        async mounted() {
            if (process.browser) {
                const options = this.options
                const parent = this.$refs['container'];

                const Module = await import('@google/model-viewer');
                const element = new Module.ModelViewerElement();

                // console.log({element})

                Object.entries(options).forEach((entry) => {
                    const name = entry[0]
                    const value = entry[1]

                    element[name] = value
                })

                parent.appendChild(element)
            }
        },

        methods: {
            enterAR() {
                const viewer = this.$refs.container.children[0]
                viewer.activateAR()
            }
        }
    };
</script>

<style scoped>
    .container {
        height: 100vh;
        width: 100vw;
    }

    .container::v-deep > * {
        height: 100%;
        width: 100%;
    }
</style>
