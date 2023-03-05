<script>
    import SectionContainer from "./SectionContainer.vue";

    export default {
        name: "AppMain",
        components: {
            SectionContainer
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
                        isCaption: true
                    },
                    {
                        secondaryTitle: 'Portfolio',
                        mainTitleFirstWord: 'latest',
                        mainTitleRest: 'work',
                        caption: '',
                        isCaption: false
                    },
                    {
                        secondaryTitle: 'Price List',
                        mainTitleFirstWord: 'Our',
                        mainTitleRest: 'Pricing',
                        caption: 'When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface.',
                        isCaption: true
                    },
                    {
                        secondaryTitle: 'Blog',
                        mainTitleFirstWord: 'Latest',
                        mainTitleRest: 'Posts',
                        caption: 'When, while the lovely valley teems with vapour around meand the',
                        isCaption: true
                    },
                    {
                        secondaryTitle: 'Testimonial',
                        mainTitleFirstWord: 'What',
                        mainTitleRest: 'People Say',
                        caption: 'When, while the lovely valley teems with vapour around meand the',
                        isCaption: true
                    }
                ]
            }
        }

    }
</script>

<template>
    <!-- sezione what we do ---------------------------------------------------------------------->
    <SectionContainer :sectionHeaders='sectionHeaders[0]' />
</template>

<style lang="scss" scoped>
</style>