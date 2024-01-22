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
      <img :src="card.card_images[0].image_url" :alt="card.name">Foto
    </div>
    <h5>
      {{ card.name }}
    </h5>
    <div>
      {{ card.type }}
    </div>
  </div>


  
</template>

<style lang="scss" scoped>



</style>
