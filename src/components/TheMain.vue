<template>
    <div>
        <main>
            <div class="container">
                <div class="row row-cols-5 pt-5">
                    <div class="col" v-for="(disc, i) in discList" :key='i'>
                        <div class="my-card-song d-flex flex-column align-items-center p-4 my-2">
                            <div class="song-cover">
                                <img class="w-100" :src="disc.poster" alt="">
                            </div>
                            <h5 class="text-uppercase text-white text-center pt-3"><strong>{{disc.title}}</strong></h5>
                            <div class="info-song mt-auto">
                                <div class="artist text-secondary text-center">{{disc.author}}</div>
                                <div class="year text-secondary text-center">{{disc.year}}</div>
                            </div>
                        </div>
                    </div>
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
                discList: [],
            }
        },

        methods: {
            fetchSongList () {
                axios.get(this.apiURL)
                .then((resp) => {
                    this.discList = resp.data.response;
                });
            },
        },
        mounted () {
            this.fetchSongList();
        },
    };
</script>

<style lang="scss">
    main {
        height: 92vh;
        background-color: #1e2d3b ;

            .my-card-song {
                height: 400px;
                background-color: #2e3a46;
            }

        }

</style>