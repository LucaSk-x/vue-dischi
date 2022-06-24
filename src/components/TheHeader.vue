<template>
    <div>
        <header>
            <div class="logo-contain p-3">
                <img class="h-100" src="https://storage.googleapis.com/pr-newsroom-wp/1/2018/11/Spotify_Logo_RGB_Green.png" alt="">
            </div>
        </header>
    </div>
</template>


<script>
    export default {
        name: 'TheHeader',
    }
</script>

<style lang="scss" scoped>
    header {
        background-color: #2e3a46;
        height: 8vh;

        .logo-contain {
            height: 100%;
        }
    }
</style>