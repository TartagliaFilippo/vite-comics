<script>
export default {
  data() {
    return {
      titlesGroup: [
        "CHARACTERS",
        "COMICS",
        "MOVIES",
        "TV",
        "GAMES",
        "COLLECTIBLES",
        "VIDEOS",
        "FANS",
        "NEWS",
        "SHOP",
      ],
      pathImageLogo: "dc-logo.png",
    };
  },
};
</script>

<template>
  <div class="wrapper">
    <div class="container">
      <img :src="'../../public/img/' + pathImageLogo" alt="" />
      <ul>
        <li v-for="title of titlesGroup">
          {{ title }}
        </li>
      </ul>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.wrapper {
  background-color: white;

  .container {
    width: 80%;
    margin: 0 auto;
    display: flex;

    img {
      max-width: 100%;
      margin-right: auto;
    }

    ul {
      list-style: none;
      display: flex;
      gap: 10px;
    }
  }
}
</style>
