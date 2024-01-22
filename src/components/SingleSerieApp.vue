<script>
export default {
    data() {
      return {
      }
    },
    props: {
      series: Object,
      image: String,
      price: String,
      title: String,
      genre: String
    }
}


</script>

<template>

  <div class="card">
    <div class="img-card">
      <img :src="image" :alt="title">
    </div>
    <div>
      {{ title }}
    </div>
  </div>
  
</template>

<style lang="scss" scoped>



</style>
