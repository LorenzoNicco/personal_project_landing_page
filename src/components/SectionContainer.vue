<script>
export default {
    name: "SectionContainer",
    props: [
        "sectionHeaders"
    ]
}
</script>

<template>
    <section :class="{'text-center' : sectionHeaders.isCaption == true}">
        <h6 class="my-red-text">{{ sectionHeaders.secondaryTitle }}</h6>

        <h2 class="my-3"><span class="fw-bold">{{ sectionHeaders.mainTitleFirstWord }}</span> <span class="fw-normal">{{ sectionHeaders.mainTitleRest }}</span></h2>

        <p v-if="sectionHeaders.isCaption == true">{{ sectionHeaders.caption }}</p>
    </section>
</template>

<style lang="scss" scoped>
    .my-red-text {
        color: $red-text;
    }
</style>