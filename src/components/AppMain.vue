<script>
    import cardsAlbum from "./cardsAlbum.vue";
    import JumboSection from "./JumboSection.vue";
    import CarouselSection from "./CarouselSection.vue";

    export default {
        name: "AppMain",
        components: {
            cardsAlbum,
            JumboSection,
            CarouselSection
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
                        textCenter: true,
                        sectionNumber: 1
                    },
                    {
                        secondaryTitle: 'Portfolio',
                        mainTitleFirstWord: 'latest',
                        mainTitleRest: 'work',
                        caption: '',
                        textCenter: false,
                        sectionNumber: 2
                    },
                    {
                        secondaryTitle: 'Price List',
                        mainTitleFirstWord: 'Our',
                        mainTitleRest: 'Pricing',
                        caption: 'When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface.',
                        textCenter: true,
                        sectionNumber: 3
                    },
                    {
                        secondaryTitle: 'Blog',
                        mainTitleFirstWord: 'Latest',
                        mainTitleRest: 'Posts',
                        caption: 'When, while the lovely valley teems with vapour around meand the',
                        textCenter: true,
                        sectionNumber: 4
                    },
                    {
                        secondaryTitle: 'Testimonial',
                        mainTitleFirstWord: 'What',
                        mainTitleRest: 'People Say',
                        caption: 'When, while the lovely valley teems with vapour around meand the',
                        textCenter: true,
                        sectionNumber: 5
                    }
                ]
            }
        }

    }
</script>

<template>
    <!-- sezione what we do ---------------------------------------------------------------------->
    <section class="py-5" :class="{'text-center' : sectionHeaders[0].textCenter == true}">
        <h6 class="my-red-text mt-4">{{ sectionHeaders[0].secondaryTitle }}</h6>

        <h2 class="my-3"><span class="fw-bold">{{ sectionHeaders[0].mainTitleFirstWord }}</span> <span class="fw-normal">{{ sectionHeaders[0].mainTitleRest }}</span></h2>

        <p>{{ sectionHeaders[0].caption }}</p>

        <cardsAlbum :sectionNumber='sectionHeaders[0].sectionNumber'/>

        <div class="button-container my-red-shadow mb-4">
            <button class="my-button my-button-color-red my-margin-top">View All Services</button>
        </div>
    </section>

    <!-- jumbosection ----------------------------------------------------------------------------->
    <div class="my-bg-dark">
        <div class="container-xl">
            <JumboSection :version="version"/>
        </div>
    </div>

    <!-- sezione latest work ---------------------------------------------------------------------->
    <section class="py-5 container-xl" :class="{'text-center' : sectionHeaders[1].textCenter == true}">
        <h6 class="my-red-text mt-4">{{ sectionHeaders[1].secondaryTitle }}</h6>

        <h2 class="my-3"><span class="fw-bold">{{ sectionHeaders[1].mainTitleFirstWord }}</span> <span class="fw-normal">{{ sectionHeaders[1].mainTitleRest }}</span></h2>

        <CarouselSection />
        
    </section>
</template>


<style lang="scss" scoped>
// utilities--------------------------------------------------------------------------------------------------
    .my-button {
        @include buttonShape;
    }

    .my-button-color-red {
        background-color: $button-color-red;
        box-shadow: $button-shadow-red;
    }
    .my-red-text {
        color: $red-text;
    }

    .button-container {
        width: fit-content;
        height: 40px;
        border-radius: 30px;
        margin: 0 auto;
        margin-top: 10rem;
    }

    .my-red-shadow {
        box-shadow: 0px 0px 15px 5px rgba(255,0,0,0.50);
    }

    .my-bg-dark {
        background: $dark-bg-gradient;
        padding: 10rem 0;
    }

</style>