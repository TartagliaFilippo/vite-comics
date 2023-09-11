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
      mainFooter: [
        {
          title: "DC COMICS",
          items: [
            "Characters",
            "Comics",
            "Movies",
            "Tv",
            "Games",
            "Collectibles",
            "Videos",
            "Fans",
            "News",
          ],
        },
        { title: "SHOP", items: ["Shop DC", "Shop DC Collectibles"] },

        {
          title: "DC",
          items: [
            "Therms Of Use",
            "Privacy policy (New)",
            "Ad Choices",
            "Advertising",
            "Jobs",
            "Subscriptions",
            "Talent Workshops",
            "CPSC Certificates",
            "Ratings",
            "Shop Help",
            "Contact Us",
          ],
        },
        {
          title: "SITES",
          items: [
            "DC",
            "MAD Magazine",
            "DC Kids",
            "DC Universe",
            "DC Power visa",
          ],
        },
      ],
      bottomFooter: [
        "footer-facebook.png",
        "footer-twitter.png",
        "footer-youtube.png",
        "footer-pinterest.png",
        "footer-periscope.png",
      ],
    };
  },
};
</script>

<template>
  <div class="wrapper">
    <div class="top-footer">
      <div class="container">
        <ul>
          <li v-for="item in topFooter">
            <div class="buy-image">
              <img :src="'../../public/img/' + item.image" alt="" />
            </div>

            <div class="text">{{ item.description }}</div>
          </li>
        </ul>
      </div>
    </div>
    <div class="main-footer">
      <div class="container">
        <div class="col">
          <h2>{{ mainFooter[0].title }}</h2>
          <ul>
            <li v-for="item in mainFooter[0].items">{{ item }}</li>
          </ul>
          <h2>{{ mainFooter[1].title }}</h2>
          <ul>
            <li v-for="item in mainFooter[1].items">{{ item }}</li>
          </ul>
        </div>
        <div class="col">
          <h2>{{ mainFooter[2].title }}</h2>
          <ul>
            <li v-for="item in mainFooter[2].items">{{ item }}</li>
          </ul>
        </div>
        <div class="col">
          <h2>{{ mainFooter[3].title }}</h2>
          <ul>
            <li v-for="item in mainFooter[3].items">{{ item }}</li>
          </ul>
        </div>
      </div>
    </div>
    <div class="bottom-footer">
      <div class="container">
        <div class="button">
          <h3>SIGN-UP NOW!</h3>
        </div>
        <div class="social">
          <h1>FOLLOW US</h1>
          <ul>
            <li v-for="image in bottomFooter">
              <img :src="'../../public/img/' + image" alt="" />
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.wrapper {
  background-color: #0282f9;
  display: flex;
  flex-direction: column;

  .top-footer {
    margin: 20px 0;
    .container {
      width: 80%;
      margin: 0 auto;

      ul {
        display: flex;
        align-items: center;
        justify-content: space-around;

        li {
          list-style: none;
          display: flex;
          align-items: center;

          .buy-image {
            width: 40px;
            height: 40px;
            display: flex;
            align-items: center;
            gap: 5px;

            img {
              max-width: 100%;
              max-height: 100%;
            }
          }
          .text {
            font-size: 10px;
            color: white;
          }
        }
      }
    }
  }
  .main-footer {
    background-image: url("../../public/img/footer-bg.jpg");

    .container {
      width: 80%;
      color: white;
      margin: 30px auto;
      display: flex;
      gap: 30px;

      ul {
        list-style: none;
        padding: 0;

        li {
          color: #6a7e80;
          font-size: 12px;
        }
      }
    }
  }
  .bottom-footer {
    background-color: #303030;

    .container {
      width: 80%;
      margin: 20px auto;

      display: flex;
      justify-content: space-between;
      align-items: center;

      .button {
        font-size: 14px;
        height: 40px;
        width: 15%;
        padding: 3px 5px;
        border: 3px solid #097ff9;
        color: white;

        display: flex;
        align-items: center;
        justify-content: center;
      }

      .social {
        display: flex;
        justify-content: flex-end;
        align-items: center;

        h1 {
          font-size: 20px;
          color: #097ff9;
          margin-right: 20px;
        }

        ul {
          list-style: none;
          display: flex;
          gap: 15px;

          li {
            width: 28px;
            display: flex;
            align-items: center;

            img {
              max-width: 100%;
            }
          }
        }
      }
    }
  }
}
</style>
