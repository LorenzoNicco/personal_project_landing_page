<script>
export default {
    name: "JumboSection"
}
</script>

<template>
    <section class="row py-4">
        <div class="col-5 d-flex flex-column justify-content-center">
            <h1 class="text-white">
                <span>Business Planning</span><br>
                <span class="fw-light">Digital Technology</span><br>
                <span>Modern Solution!</span>
            </h1>
            
            <p class="my-text-color-blue my-5">When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface.</p>
            
            <div>
                <button class="my-button my-button-color-red me-3">Try it Now</button>
                
                <button class="my-button my-button-color-blue">Explore More</button>
            </div>
        </div>

        <div class="col-7">
            <img src="../assets/corporate-landing/images/header.png" alt="img not found" class="w-100">
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

</style>