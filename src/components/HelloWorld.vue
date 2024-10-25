<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div class="carousel-container">
      <el-carousel :interval="5000" type="card" height="200px">
        <el-carousel-item v-for="(item, index) in items" :key="index">
          <img src="../assets/image2.jpg" class="carousel-image" />
        </el-carousel-item>
      </el-carousel>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      items: [{}, {}, {}, {}, {}]
    }
  }
}
</script>

<style scoped>
.carousel-container {
  margin: 20px auto;
  max-width: 800px;
}

.carousel-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>
