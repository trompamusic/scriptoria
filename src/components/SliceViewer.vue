<template>
    <img v-if="sliceFile" :src="require(`@/assets${sliceFile}`)">
    <!-- sliceType: measures, lines, pages -> @/assets/omr_files/slices/sliceType/sliceFile -->
</template>

<script>
export default {
    name: "SliceViewer",
    props: {
        sliceFile: {
            type: String,
            required: true,
            default: ""
        }
    }
}
</script>

<style lang="scss" scoped>
    img {
        border-radius: 5px;
        border: 5px solid #DFE3E8;
        box-sizing: border-box;
    }
</style>