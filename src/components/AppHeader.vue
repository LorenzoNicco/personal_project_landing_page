<script>
    export default {
        name: "AppHeader",
        data () {
            return {
                headerMenu: [
                    'Home',
                    'About',
                    'Services',
                    'Blog',
                    'Contact',
                    'Portfolio'
                ]
            }
        }

    }
</script>

<template>
    <header>
        <div class="container-xl">
            <div class="row">
                <div class="col">
                    <img src="../assets/corporate-landing/images/white-logo-2.png" alt="">
                </div>

                <nav class="col d-flex">
                    <ul class="d-flex">
                        <li v-for="menuVoice in headerMenu">
                            <a href="#" class="text-decoration-none text-black">{{ menuVoice }}</a>
                        </li>
                    </ul>

                    <button class="my-button">Sign In</button>
                </nav>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
    nav {
        ul {
            list-style: none;

        }

        .my-button {
            @include buttonShape;
        }
    }
</style>
