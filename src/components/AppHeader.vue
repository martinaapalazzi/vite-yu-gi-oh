<script>
import logo from '../assets/img/dc-logo.png';
  export default {
    data() {
      return {
        logo,
        linksHeader: [
          {
            label: 'CHARACTERS'
          },
          {
            label: 'COMICS'
          },
          {
            label: 'MOVIES'
          },
          {
            label: 'TV'
          },
          {
            label: 'GAMES'
          },
          {
            label: 'COLLECTIBLES'
          },
          {
            label: 'VIDEOS'
          },
          {
            label: 'FANS'
          },
          {
            label: 'NEWS'
          },
          {
            label: 'SHOP'
          },

        ]
      }
    },
  }
</script>

<template>

  <div id="header">

    <div class="container">

      <div class="header-container">

        <div class="logo-container">
          <img :src="logo" alt="Logo">
        </div>

        <div>
          <ul>
            <li v-for="(singleLabel, index) in linksHeader">
              <a v-if="singleLabel.active ? 'active' : ' '"
              :class="{
                'active': singleLabel.active
              }"
              href="#"> {{ singleLabel.label }}</a>
            </li>
          </ul>
        </div>

      </div>

    </div>

  </div>
  
</template>

<style lang="scss" scoped>

</style>
