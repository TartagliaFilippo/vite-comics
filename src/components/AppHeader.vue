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
        <li v-for="title in titlesGroup">
          {{ title }}
        </li>
      </ul>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.wrapper {
  background-color: white;
  margin: 10px 0;

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
      align-items: center;
      gap: 10px;
      font-weight: bold;

      li {
        cursor: pointer;

        &:hover {
          box-shadow: 0px 52px 0px -4px #0282f9;
        }
      }
    }
  }
}
</style>
