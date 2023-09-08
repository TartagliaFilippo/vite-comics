<script>
export default {
  data() {
    return {
      topFooter: [
        {
          image: "buy-comics-digital-comics.png",
          description: "DIGITAL COMICS",
        },
        {
          image: "buy-comics-merchandise.png",
          description: "DC MERCHANDISE",
        },
        {
          image: "buy-comics-subscriptions.png",
          description: "SUBSCRIPTION",
        },
        {
          image: "buy-comics-shop-locator.png",
          description: "COMIC SHOP LOCATOR",
        },
        {
          image: "buy-dc-power-visa.svg",
          description: "DC POWER VISA",
        },
      ],
    };
  },
};
</script>

<template>
  <div class="wrapper">
    <div class="container">
      <div class="top-footer">
        <ul>
          <li v-for="item of topFooter">
            <div class="buy-image">
              <img :src="'../../public/img/' + item.image" alt="" />
            </div>

            <div class="text">{{ item.description }}</div>
          </li>
        </ul>
      </div>
      <div class="main-footer">
        <div class="col">
          <h2></h2>
          <ul>
            <li></li>
          </ul>
          <h2></h2>
          <ul>
            <li></li>
          </ul>
        </div>
        <div class="col">
          <h2></h2>
          <ul>
            <li></li>
          </ul>
        </div>
        <div class="col">
          <h2></h2>
          <ul>
            <li></li>
          </ul>
        </div>
      </div>
      <div class="bottom-footer">
        <div class="button"></div>
        <div class="social">
          <h1>FOLLOW</h1>
          <ul>
            <li></li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.wrapper {
  background-color: #0282f9;

  .container {
    width: 80%;
    margin: 0 auto;

    ul {
      display: flex;
      align-items: center;
      justify-content: space-between;

      li {
        list-style: none;
        display: flex;
        align-items: center;

        .buy-image {
          width: 50px;
          height: 50px;
          display: flex;
          align-items: center;

          img {
            max-width: 100%;
            max-height: 100%;
          }
        }
        .text {
          font-size: 12px;
        }
      }
    }
  }
}
</style>
