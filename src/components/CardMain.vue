<script>
export default {
  props: {
    item: Object,
  },
};
</script>

<template>
  <div class="card">
    <div class="image">
      <img :src="item.thumb" alt="" />
    </div>
    <div class="title-cartoon">
      <h4>{{ item.series }}</h4>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.card {
  width: 120px;
  height: 150px;
  color: white;
  margin-bottom: 30px;

  img {
    max-width: 100%;
    aspect-ratio: 1;
  }
}
</style>
