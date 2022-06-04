<template>
    <main>
        <section class="container">
            <h1>Vídeos</h1>
            <section class="videos">
                <div v-for="(video,index) in videos" :key="index" class="video">
                    <a  :href="video.link">
                        <img :src="video.thumb" :alt="video.title">
                        <div class="video-text">{{ video.title }}</div>
                    </a>
                </div>
            </section>

        </section>
    </main>
</template>

<script>
import api from '@/services/api.js'
export default {
    name: 'VideosMain',
    data(){
        return{
            videos: []
        }
    },
    mounted(){
        api.get('/videos.json').then(response =>{
            this.videos = response.data
        })
    }
}
</script>

<style scoped>
 main{
     align-items: center;
 }
 .videos{
     display: flex;
     flex-direction: column;
     align-items: center;
 }
 .video{
     width: 80%;
     margin-bottom: 30px;
 }
 .video img{
     width: 100%;
 }

</style>