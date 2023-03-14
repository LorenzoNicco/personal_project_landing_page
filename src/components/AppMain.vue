<script>
    import cardsAlbum from "./cardsAlbum.vue";

    export default {
        name: "AppMain",
        components: {
            cardsAlbum
        },
        data() {
            return {
                version: 'main',
                sectionHeaders: [
                    {
                        secondaryTitle: 'Our Services',
                        mainTitleFirstWord: 'What',
                        mainTitleRest: 'We Do',
                        caption: 'When, while the lovely valley teems with vapour around meand the',
                        isCaption: true,
                        sectionNumber: 1
                    },
                    {
                        secondaryTitle: 'Portfolio',
                        mainTitleFirstWord: 'latest',
                        mainTitleRest: 'work',
                        caption: '',
                        isCaption: false,
                        sectionNumber: 2
                    },
                    {
                        secondaryTitle: 'Price List',
                        mainTitleFirstWord: 'Our',
                        mainTitleRest: 'Pricing',
                        caption: 'When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface.',
                        isCaption: true,
                        sectionNumber: 3
                    },
                    {
                        secondaryTitle: 'Blog',
                        mainTitleFirstWord: 'Latest',
                        mainTitleRest: 'Posts',
                        caption: 'When, while the lovely valley teems with vapour around meand the',
                        isCaption: true,
                        sectionNumber: 4
                    },
                    {
                        secondaryTitle: 'Testimonial',
                        mainTitleFirstWord: 'What',
                        mainTitleRest: 'People Say',
                        caption: 'When, while the lovely valley teems with vapour around meand the',
                        isCaption: true,
                        sectionNumber: 5
                    }
                ]
            }
        }

    }
</script>

<template>
    <!-- sezione what we do ---------------------------------------------------------------------->
    <section :class="{'text-center' : sectionHeaders[0].isCaption == true}">
        <h6 class="my-red-text">{{ sectionHeaders[0].secondaryTitle }}</h6>

        <h2 class="my-3"><span class="fw-bold">{{ sectionHeaders[0].mainTitleFirstWord }}</span> <span class="fw-normal">{{ sectionHeaders[0].mainTitleRest }}</span></h2>

        <p v-if="sectionHeaders[0].isCaption == true">{{ sectionHeaders[0].caption }}</p>

        <cardsAlbum :sectionNumber='sectionHeaders[0].sectionNumber'/>
    </section>
</template>

<style lang="scss" scoped>
    .my-red-text {
        color: $red-text;
    }
</style>