<script>
export default {
    name: "cardsAlbum",
    data() {
        return {
            cardsContent: {
                whatWeDo: [
                    {
                        pic: "./src/assets/corporate-landing/images/Group-247.png",
                        title: "Data Analysis",
                        paragraphe: "When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper"
                    },
                    {
                        pic: "./src/assets/corporate-landing/images/Group-567.png",
                        title: "SEO Optimization",
                        paragraphe: "When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper"
                    },
                    {
                        pic: "./src/assets/corporate-landing/images/Group-538.png",
                        title: "Security Data",
                        paragraphe: "When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper"
                    },
                    {
                        pic: "./src/assets/corporate-landing/images/Group-566.png",
                        title: "Branding Strategy",
                        paragraphe: "When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper"
                    }
                ]

            }

        }
    },
    props: [
        "sectionNumber"
    ]
}
</script>

<template>
    <!-- sezione what we do -------------------------------------------------------------------------------->
    <div v-if="sectionNumber == 1" class="container-xl my-card-container">
        <div class="row">
            <div class="col-3" v-for="card in cardsContent.whatWeDo">
                <div class="my-pic-container mb-5">
                    <img :src="card.pic" alt="">
                </div>

                <h4 class="mb-4 fw-bold">{{ card.title }}</h4>

                <p>{{ card.paragraphe }}</p>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>

// sezione what we do-------------------------------------------------------------------------------
    .my-card-container {
        margin-top: 8rem;

        .my-pic-container {
            height: 8rem;
    
            img {
                height: 100%;
            }
        }

        p {
            width: 80%;
            margin-left: 10%;
        }
    }
</style>