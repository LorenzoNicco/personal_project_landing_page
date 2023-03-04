<script>
    export default {
        name: "AppHeader",
        data () {
            return {
                headerMenu: [
                    {
                        menuVoice: 'Home',
                        status: true
                    },
                    {
                        menuVoice: 'About',
                        status: false
                    },
                    {
                        menuVoice: 'Services',
                        status: false
                    },
                    {
                        menuVoice: 'Blog',
                        status: false
                    },             
                    {
                        menuVoice: 'Contact',
                        status: false
                    },
                    {
                        menuVoice: 'Portfolio',
                        status: false
                    },
                ]
            }
        }

    }
</script>

<template>
    <header class="my-bg-dark">
        <div class="container-xl">
            <div class="row pt-3">
                <div class="col">
                    <img src="../assets/corporate-landing/images/white-logo-2.png" alt="">
                </div>

                <nav class="col d-flex justify-content-between">
                    <ul class="d-flex mb-0">
                        <li v-for="menuIndex in headerMenu" class="px-2 pt-3">
                            <a href="#" class="text-decoration-none" v-bind:class="menuIndex.status == true ? 'active' : 'text-light'">{{ menuIndex.menuVoice }}</a>
                        </li>
                    </ul>

                    <button class="my-button my-button-color-blue mt-2">Sign In</button>
                </nav>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
    .my-bg-dark {
        background: $dark-bg-gradient;
    }

    nav {
        ul {
            list-style: none;

            .active {
                color: #f9636b
            }

        }

        .my-button {
            @include buttonShape;
        }

        .my-button-color-blue {
            background-color: $button-color-blue;
            box-shadow: $button-shadow-blue;
        }
    }

</style>
