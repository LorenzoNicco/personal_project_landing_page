<script>
export default {
    name: "JumboSection",
    props: [
        'version'
    ]
}
</script>

<template>
    <section class="row" :class="{'flex-row-reverse' : version == 'main'}">
        <div class="col-5 d-flex flex-column justify-content-center">
            <h1 class="text-white mb-0" v-if="version == 'header'">
                <span>Business Planning</span><br>
                <span class="fw-light">Digital Technology</span><br>
                <span>Modern Solution!</span>
            </h1>
            <div v-else-if="version == 'main'">
                <h4 class="text-white">Start Your Project</h4>

                <h2 class="text-white mt-3 mb-0 fs-1">
                    <span>GROW YOUR BUSINESS</span><br>
                    <span class="fw-light">WITH OUR STRATEGY</span>
                </h2>
            </div>
            
            <p class="my-text-color-blue my-5" v-if="version == 'header'">When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface.</p>
            <p class="my-text-color-blue my-5" v-else-if="version == 'main'">When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface.of the impenetrable foliage of my trees, and but a few stray gleams steal into the inner sanctuary.</p>
            
            <div>
                <button class="my-button my-button-color-red me-3">Try it Now</button>
                
                <button class="my-button my-button-color-blue">Explore More</button>
            </div>
        </div>

        <div class="col-7 d-flex justify-content-start align-items-center">
            <img v-if="version == 'header'" src="../assets/corporate-landing/images/header.png" alt="img not found" class="w-100">
            <div  v-else-if="version == 'main'" class="my-img-container-jumbo">
                <img src="../assets/corporate-landing/images/men-data.png" alt="img not found" class="w-100 position-absolute my-z-index-20">
                <img src="../assets/corporate-landing/images/nemoodar.png" alt="img not found" class="w-100 my-translate">
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    .my-text-color-blue {
        color: #03a7d3a6
    }

    .my-button {
        @include buttonShape;
    }

    .my-button-color-red {
        background-color: $button-color-red;
        box-shadow: $button-shadow-red;
    }

    .my-button-color-blue {
        background-color: $button-color-blue;
        box-shadow: $button-shadow-blue;
    }

    .my-translate {
        transform: translateY(-20%);
    }

    .my-z-index-20 {
        z-index: 20;
    }

    .my-img-container-jumbo {
        width: 60%;
        position: relative;
    }

</style>