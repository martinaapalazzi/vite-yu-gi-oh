<script>

import SingleSerieApp from './SingleSerieApp.vue';

  export default {
    data() {
      return {
        navMenu: [
          {
            img: './src/assets/img/buy-comics-digital-comics.png',
            name: "DIGITAL COMICS"
          },
          {
            img: './src/assets/img/buy-comics-merchandise.png',
            name: "DC MERCHINDISE"
          },
          {
            img: './src/assets/img/buy-comics-shop-locator.png',
            name: "COMICS SHOP LOCATOR"
          },
          {
            img: './src/assets/img/buy-comics-subscriptions.png',
            name: "SUBSCRIPTION"
          },
          {
            img: './src/assets/img/buy-comics-subscriptions.png',
            name: "DC POWER VISA"
          },
        ],
        series: [
          {
            "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
            "price": "$19.99",
            "series": "ACTION COMICS",
            "type": "comic book"
          },
          {
            "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
            "price": "$3.99",
            "series": "AMERICA VAMPIRE 1976",
            "type": "comic book"
          },
          {
            "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
            "price": "$16.99",
            "series": "AQUAMAN",
            "type": "graphic novel"
          },
          {
            "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
            "price": "$2.99",
            "series": "BATGIRL",
            "type": "comic book"
          },
          {
            "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
            "price": "$3.99",
            "series": "BATMAN",
            "type": "comic book"
          },
          {
            "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
            "price": "$2.99",
            "series": "BATMAN BEYOND",
            "type": "comic book"
          },
          {
            "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
            "price": "$3.99",
            "series": "BATMAN/SUPERMAN",
            "type": "comic book"
          },
          {
            "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
            "price": "$4.99",
            "series": "BATMAN/SUPERMAN ANNUAL",
            "type": "comic book"
          },
          {
            "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
            "price": "$5.99",
            "series": "BATMAN: THE JOKER WAR ZONE",
            "type": "comic book"
          },
          {
            "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
            "price": "$6.99",
            "series": "BATMAN: THREE JOKERS",
            "type": "comic book"
          },
          {
            "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
            "price": "$4.99",
            "series": "BATMAN: WHITE KNIGHT PRESENTS: HARLEY QUINN",
            "type": "comic book"
          },
          {
            "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
            "price": "$16.99",
            "series": "CATWOMAN",
            "type": "graphic novel"
          }
        ]
      }
    },
    components: {
      SingleSerieApp
    }
  }
</script>

<template>

  <div id="main">

    <div class="container">
      <div class="content-container">
        <div class="jumbotron">
          <img src="../assets/img/jumbotron.jpg" alt="">
        </div>
        <div class="current-series">
          <span>
            CURRENT SERIES
          </span>
          <div class="series-container">
            <SingleSerieApp 
              style="color: white;"
              v-for="(serie, index) in series"
              :title="serie.series"
              :price="serie.price"
              :image="serie.thumb"/>
            <div>
              <button>
                LOAD MORE
              </button>
            </div>
          </div>
        </div>
      </div>

      <div class="second-container">
        <div class="row" v-for="(nav, index) in navMenu">
          <div>
            <img :src="nav.img" alt="nav.name">
          </div>
          <a href="#">
            {{ nav.name }}
          </a>
        </div>
      </div>

    </div>
    
  </div>
  
</template>

<style lang="scss" scoped>

</style>
