<template>
    <div class="container">
        <div class="header">
            <h1 class="header-title">Cinema XXI</h1>
            <h3 class="header-subtitle">Find your best movie here</h3>
        </div>
        <div class="movie" v-for="(data, index) in movie" :value="data" :key="index">
            <div class="movie-item" @click="detailfilm(data.id)">
                <img v-bind:src="data.image" class="img-fluid img-movie" v-bind:alt="data">
            </div>
        </div>
        <div class="footer">
            <h5>Copyright &copy;2020. Created by Berliana Aliftia Ifada. All rights reserved</h5>
        </div>
    </div>
</template>
<script>
import Img1 from '../assets/movie/001.jpg'
import Img2 from '../assets/movie/002.jpg'
import Img3 from '../assets/movie/003.jpg'
import Img4 from '../assets/movie/004.jpg'
import Img5 from '../assets/movie/005.jpg'
import Img6 from '../assets/movie/006.jpg'
import Img7 from '../assets/movie/008.jpg'
import Img8 from '../assets/movie/009.jpg'

export default {
  data: () => ({
    movie: [
      { id: 1, image: Img1 },
      { id: 2, image: Img2 },
      { id: 3, image: Img3 },
      { id: 4, image: Img4 },
      { id: 5, image: Img5 },
      { id: 6, image: Img6 },
      { id: 7, image: Img7 },
      { id: 8, image: Img8 }
    ]
  }),
  methods: {
    detailfilm (filmId) {
      this.$router.push({ name: 'detail', params: { id: filmId } })
    }
  }
}
</script>
<style scoped>
    .container {
        width: auto;
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        grid-auto-rows: minmax(50px, auto);
    }
    .header {
        padding: 50px;
        grid-column: 1/5;
        background-color: #1abc9c;
        color: #fff;
        text-align: left;
    }
    .header-title {
      font-family: monospace;
      font-size: 70px;
      color: #34495e;
    }
    .header-subtitle {
        font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
        font-size: 20px;
        color: #fff;
    }
    .footer {
        padding: 10px;
        grid-column: 1/5;
        background-color: #404040;
        color: #fff;
        text-align: center;
    }
    .movie {
        padding-top: 60px;
        padding-bottom: 60px;
        text-align: center;
        background-color: #ededed;
    }
    .img-movie {
        width: 250px;
        box-shadow: 0 20px 35px 0 rgba(0,0,0,0.2);
        transition: 0.3s ease;
    }
    .img-movie:hover{
        box-shadow: 0 40px 45px 0 rgba(0,0,0,0.2);
    }
</style>
