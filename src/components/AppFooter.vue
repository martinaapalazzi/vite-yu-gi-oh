<script>
  export default {
    data() {
      return {
        dcComicsSections: [
          {
            section: 'Characters'
          },
          {
            section: 'Comics'
          },
          {
            section: 'Movies'
          },
          {
            section: 'TV'
          },
          {
            section: 'Games'
          },
          {
            section: 'Videos'
          },
          {
            section: 'News'
          }
        ],
        Shops: [
          {
            shop: 'Shop DC'
          },
          {
            shop: 'Shop DC Collectibles'
          },
        ],
        Dc: [
          {
            link:'Terms of use',
          },
          {
            link:'Privacy politicy(New)',
          },
          {
            link:'Ad Choices',
          },
          {
            link:'Advertising',
          },
          {
            link:'Jobs',
          },
          {
            link:'Subscriptions',
          },
          {
            link:'Talent Workshops',
          },
          {
            link:'Cpsc certificates',
          },
          {
            link:'Ratings',
          },
          {
            link:'Shop help',
          }, 
          {
            link:'Contact us',
          },
        ],
        Sites: [
          {
            site:'Dc',
          },
          {
            site:'Mad magazine',
          },
          {
            site:'Dc kids',
          },
          {
            site:'Dc universe',
          },
          {
            site:'Dc power visa',
          },
        ],
        
        
      }
    },
  }
</script>

<template>
  
  <div id="footer">

    <div class="top-footer">

      <div class="first-column">
        
        <h4> 
          DC COMICS
        </h4>
        <div v-for="(section, index) in dcComicsSections">
          <a href="#">
            {{ section.section }}
          </a>
        </div>

        <br>

        <h4> 
          SHOP
        </h4>
        <div v-for="(shop, index) in Shops">
          <a href="#">
            {{ shop.shop }}
          </a>
        </div>

      </div>

      <div class="second-column">

        <h4> 
          DC
        </h4>
        <div v-for="(link, index) in Dc">
          <a href="#">
            {{ link.link }}
          </a>
        </div>

      </div>

      <div class="third-column">

        <h4> 
          SITES
        </h4>
        <div v-for="(site, index) in Sites">
          <a href="#">
            {{ site.site }}
          </a>
        </div>

      </div>

      <div class="special-logo">
        <img src="../assets/img/dc-logo-bg.png" alt="">
      </div>

    </div>

    <div class="bottom-footer">

      <button>
        SIGN-UP NOW!
      </button>

      <div class="right-side-footer">
        <h3>
          FOLLOW US
        </h3>
        <div class="apps-container">
          <img class="single-app" src="../assets/img/footer-facebook.png" alt="../assets/img/footer-facebook.png">
          <img src="../assets/img/footer-twitter.png" alt="../assets/img/footer-twitter.png">
          <img src="../assets/img/footer-youtube.png" alt="../assets/img/footer-youtube.png">
          <img src="../assets/img/footer-pinterest.png" alt="../assets/img/footer-pinterest.png">
          <img src="../assets/img/footer-periscope.png" alt="../assets/img/footer-periscope.png">
        </div>
      </div>

    </div>

  </div>
  
</template>

<style lang="scss" scoped>

</style>
