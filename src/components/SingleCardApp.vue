<script>
export default {
    data() {
      return {
      }
    },
    props: {
      card: Object
    }
}

</script>

<template>

  <div class="single-card">
    <div>
      <img :src="card.card_images[0].image_url" :alt="card.name">
    </div>
    <h6 class="text-white text-uppercase">
      {{ card.name }}
    </h6>
    <div>
      {{ card.type }}
    </div>
  </div>


  
</template>

<style lang="scss" scoped>



</style>
