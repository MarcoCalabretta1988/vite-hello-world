<script>
export default {
    data() {
        return {
            imgName: 'banner.png'
        }

    },
    methods: {
        buildImagePatch() {
            const url = new URL(`../assets/${this.imgName}`, import.meta.url)
            return url.href
        }
    }
}
</script>

<template>
    <img :src="buildImagePatch()" alt="">
</template>