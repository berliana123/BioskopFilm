<template>
    <div class="container">
        <div class="header">
            <h1 class="header-title">Cinema XXI</h1>
            <h3 class="header-subtitle">Find your best movie here</h3>
        </div>
        <div class="movie" v-for="(data, index) in movie" :value="data" :key="index">
            <div class="movie-item" v-if="filmId == data.id">
                <h1 class="page-title">Movie Details</h1>
                <img v-bind:src="data.image"  class="img-fluid img-movie" v-bind:alt="data">
                <div>
                    <h1>{{data.title}}</h1>
                    <h2>IMDb : {{data.rating}}</h2>
                    <h4>{{data.release}} | {{data.duration}} | {{data.genre}} | {{data.age}}</h4>
                    <br/><br/>
                    <p>Director : {{data.director}}</p>
                    <p>Cast by : {{data.cast}}</p>
                    <h4>SYNOPSYS</h4>
                    <p class="desc">{{data.desc}}</p>
                </div>
            </div>
        </div>
        <div class="back">
            <router-link to='/'><button class="btn-back">BACK TO HOME</button></router-link>
        </div>
        <div class="footer">
            <h5>Copyright &copy;2020. Created by Berliana Aliftia. All rights reserved</h5>
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
  data () {
    return {
      filmId: this.$route.params.id,
      movie: [
        {
          id: 1,
          image: Img1,
          title: 'Sonic the Hedgehog',
          rating: '4,7/5',
          release: '25 February 2020',
          duration: '1 hrs 39 mins',
          genre: 'ACTION, ADVENTURE, FAMILY, SCI-FI',
          age: '17+',
          director: 'Jeff Fowler',
          cast: 'James Marsden, Ben Schwartz, Tika Sumpter, Natasha Rothwell, Neal McDonough, Adam Pally, Jim Carrey.',
          desc: 'Sonic the Hedgehog merupakan film aksi petualngan yang disutradarai oleh Jeff Fowler. Setelah menemukan landak kecil berwarna biru dan berlari sangat cepat, Tom Wachowski (James Marsden) seorang perwira polisi kota kecil harus membantunya mengalahkan Dr. Ivo Robotnik (Jim Carrey) yang ingin melakukan percobaan kepadanya.'
        },
        {
          id: 2,
          image: Img2,
          title: 'Sebelum Iblis Menjemput: Ayat 2',
          rating: '8,6/10',
          release: '27 Feb 2020',
          duration: '1 hrs 50 mins',
          genre: 'HORROR',
          age: '17+',
          director: 'Timo Tjahjanto',
          cast: 'Chelsea Islan, Baskara Mahendra, Widika Sidmore, Hadijah Shahab, Lutesha, Arya Vasco, Aurelie Moeremans, Karina Salim, Shareefa Daanish',
          desc: 'Sebelum Iblis Menjemput Ayat 2 merupakan film horor yang disutradarai oleh Timo Tjahjanto. Dua tahun setelah lepas dari teror iblis, Alfie (Chelsea Islan) dan Nara (Hadijah Shahab) mencoba melanjutkan kehidupan mereka. Namun Alfie masih terus dihantui perasaan bersalah dan penglihatan tidak wajar. Mimpi terburuk Alfie nyatanya baru dimulai dan bahaya yang menunggu semakin mengancam, sosok kegelapan yang begitu haus akan jiwa bangkit untuk menjemput nyawa mereka.'
        },
        {
          id: 3,
          image: Img3,
          title: 'The Invisible Man',
          rating: '8,6/10',
          release: '26 Feb 2020',
          duration: '2 hrs 05 mins',
          genre: 'Thriller',
          age: '17+',
          director: 'Leigh Whannell.',
          cast: 'Joaquin Phoenix, Robert De Niro, Zazie Beetz, and many more.',
          desc: 'Before the show goes live, Arthur requests that Murray introduce him as Joker, a reference to Murrays previous mockery. Arthur walks out to applause, but starts telling morbid jokes, confesses to the train murders, and rants about how society abandons the downtrodden and mentally ill. Arthur kills Murray and is arrested as riots break out across Gotham. One rioter corners the Wayne family in an alley and murders Thomas and his wife, Martha, sparing Bruce. Rioters in an ambulance crash into the police car carrying Arthur, freeing him, he dances to the cheers of the crowd.'
        },
        {
          id: 4,
          image: Img4,
          title: 'Teman Tapi Menikah 2',
          rating: '8,5/10',
          release: '27 Feb 2020',
          duration: '1h 30 min',
          genre: 'DRAMA',
          age: '17+',
          director: 'Rako Prijanto',
          cast: 'Adipati Dolken, Mawar De Jongh, Vonny Cornellya, Sari Nila, Ivan Leonardy, Clay Gribble, Sarah Sechan, Jourdy Pranata, Tubagus Ali, Ravil Prasetya, Narga Kautsar, Canti Tachril, Thalia Basir, Lili SP.',
          desc: 'Teman Tapi Menikah 2 merupakan film drama romantis yang disutradarai oleh Rako Prijanto. Belum puas menikmati momen sebagai pasangan baru, Ayu tiba-tiba hamil. Kepribadiannya berubah total. Dari yang tadinya semangat nemenin Ditto ke mana-mana, ia jadi mager dan parahnya, super sensitif! Ditto pun harus menahan diri dan pura-pura tidak cemburu dengan perhatian yang Ayu berikan ke si janin. Pertengkaran yang sering terjadi membuat Ayu dan Ditto harus memilih mana yang mau dipertahankan; pernikahan mereka atau si bayi?'
        },
        {
          id: 5,
          image: Img5,
          title: 'The Call of the Wild',
          rating: '4,6/5',
          release: '21 Feb 2020',
          duration: '1 hrs 40 mins',
          genre: 'ADVENTURE,ANIMATION,DRAMA',
          age: '17+',
          director: 'Chris Sanders',
          cast: 'Erwin Stoff, dengan Diana Pokorny sebagai produser eksekutif dan Ryan Stafford sebagai co-produser dan produser efek visual. The Call of the Wild dibintangi Harrison Ford, Dan Stevens, Omar Sy, Karen Gillan, Bradley Whitford, dan Colin Woodell.',
          desc: 'The Call of the Wild merupakan film petualangan, drama, keluarga yang disutradarai oleh Chris Sanders. Diadaptasi dari kisah sastra klasik kesayangan, The Call of the Wild berkisah tentang Buck, seekor anjing peliharaan berhati besar yang hidupnya berubah 180 derajat ketika dia tiba-tiba diculik dari rumahnya di California dan dipindahkan ke belantara eksotis Yukon Alaska pada masa Demam Emas Klondike di tahun 1890-an. Buck menjadi pendatang baru di regu anjing penarik kereta salju pengiriman surat - dan kemudian menjadi pemimpinnya - Buck mengalami petualangan yang tidak terlupakan, hingga akhirnya menemukan tempat sejatinya di dunia dan menjadi tuan atas dirinya sendiri.'
        },
        {
          id: 6,
          image: Img6,
          title: 'The Gentlemen',
          rating: '4/5',
          release: '19 Feb 2020',
          duration: '1 hrs 53 mins',
          genre: 'Action',
          age: '17+',
          director: 'The Gentlemen',
          cast: 'Matthew McConaughey, Charlie Hunnam, Henry Golding, Colin Farrell, Hugh Grant.',
          desc: 'THE GENTLEMEN merupakan film aksi yang disutradarai oleh Guy Ritchie. Film The Gentlemen mengisahkan seorang ekspatriat Mickey Pearson yang membangun sebuah bisnis mariyuana yang sangat menguntungkan di London. Ketika tersiar kabar bahwa Mickey bermaksud menjual seluruh bisnisnya, muncullah berbagai intik, siasat, suap menyuap, dan pemerasan dari berbagai pihak agar dapat mencuri lahan kekuasaannya.'
        },
        {
          id: 7,
          image: Img7,
          title: 'Guns Akimbo',
          rating: '8,0/10',
          release: '28 Feb 2020',
          duration: '1 hrs 35 mins',
          genre: 'Action',
          age: '17+',
          director: 'Jason Lei Howden',
          cast: 'Daniel Radcliffe, Samara Weaving.',
          desc: 'GUNS AKIMBO merupakan film aksi yang disutradarai oleh Jason Lei Howden. Miles (Radcliffe) seorang pengembang video game, terbangun dengan pistol di baut pada tangannya. Ia menjadi peserta berikutnya dalam pertandingan mematikan di dunia nyata yang mengalir secara online. Miles harus melarikan diri dari segalanya, namun tidak akan lepas dari Nix (Weaving) seorang pembunuh dari puncak level permainan yang terus memburunya.'
        },
        {
          id: 8,
          image: Img8,
          title: 'Aku Tahu Kapan Kamu Mati',
          rating: '7,5/10',
          release: '05 Mar 2020',
          duration: '1 hrs 32 mins',
          genre: 'HORROR',
          age: '17+',
          director: 'Hadrah Daeng Ratu',
          cast: 'Natasha Wilona, Ria Ricis, Al Ghazali, Fitria Rasyidi, Sonia Alexa, Ryma Gembala, Rita Nurmaliza, Elizabeth Christine, Adinda Halona, Opie Kumis, Asri Welas, Catherine Wilson, Daus Separo.',
          desc: 'Aku Tahu Kapan Kamu Mati merupakan film horor yang disutradarai oleh Hadrah Daeng Ratu. Setelah mati suri, SIENA bisa melihat pertanda orang akan mati. SIENA ketakutan dan ingin keluar dari situasi yang mengerikan ini. FLO, NENI dan VINA sahabat SIENA tidak percaya dengan kemampuan yang tiba tiba di miliki oleh SIENA. Tapi SIENA terus meyakinkan dengan penglihatannya. Apalagi satu persatu orang di sekitarnya mati setelah SIENA melihat pertanda dengan munculnya arwah yang menjemput orang tersebut. Hingga akhirnya pertanda tersebut muncul di dekat BRAMA, kakak kelas yang di cintainya. SIENA berusaha menggagalkan kematian BRAMA yang akan menjemputnya. Ternyata bukan hanya BRAMA. SIENA juga melihat pertanda orang orang terdekatnya akan mati. SIENA berusaha menggagalkan kematian kematian itu. Hingga pertanda kematian itu sendiri datang mengancam dirinya.'
        }
      ]
    }
  }
}
</script>
<style scoped>
    .container {
        width: auto;
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
    }
    .movie-item {
        padding: 50px;
        width: auto;
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        grid-auto-rows: minmax(50px, auto);
        text-align: left;
        background-color: #ededed;
    }
    .page-title {
        grid-column: 1/3;
        text-align: center;
        padding-bottom: 30px;
        background-color: #ededed;
        color: #34495e;
        font-family: 'Times New Roman', Times, serif;
    }
    .back {
      text-align: center;
      padding-bottom: 50px;
      background-color: #ededed;
    }
    .btn-back {
        background-color: #34495e;
        color: #fff;
        border: 0px;
        border-radius: 60px;
        text-align: center;
        margin: 5px 2px;
        padding: 20px 15px;
        cursor: pointer;
        transition: 0.3s;
        margin: 20px;
        width: 300px;
    }
    .btn-back:hover {
        background-color: transparent;
        border: 2px solid #34495e;
        color: #34495e;
    }
    .img-movie {
        width: 500px;
        box-shadow: 0 20px 25px 0 rgba(0,0,0,0.2);
        transition: 0.3s ease;
    }
    .desc {
        text-align: justify;
    }
    .footer {
        padding: 10px;
        grid-column: 1/5;
        background-color: #404040;
        color: #fff;
        text-align: center;
    }
</style>
