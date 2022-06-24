<template>
    <div>
        <main>
            <div class="container">
                <div class="row row-cols-2 row-cols-md-3 row-cols-lg-4 mx-4">
                    <div class="col p-3"></div>
                </div>
            </div>
        </main>
    </div>
</template>


<script>
    import axios from "axios";

    export default {
        name: 'TheMain',

        data() {
            return {
                apiURL: 'https://flynn.boolean.careers/exercises/api/array/music',
                image: '',
                text: '',
                artist: '',
                year: '',
            }
        },

        methods: {
            fetchSongList () {
                axios.get(this.apiURL, {

                })
                .then((resp) => {
                    this.text = resp.data.response;
                    resp.response.poster;
                    resp.response.poster;
                    resp.response.poster;
                });
            }
        },
    };
</script>

<style lang="scss">
    main {
        height: 92vh;
        background-color: #1e2d3b ;

        .col {
            background-color: #2e3a46;
        }
    }
</style>