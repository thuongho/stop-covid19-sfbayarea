<template>
  <div class="TitleBar">
    <div class="Background-Wrapper">
      <div class="header-container">
        <h2 class="headertitle">
          {{ header }}
        </h2>
        <p class="headersubtitle">
          {{ subheader }}
        </p>
      </div>
      <v-card class="card">
        <h4>
          <span class="cardheader">
            Help us raise Bay Area COVID awareness.
          </span>
        </h4>
        <p>
          <span class="cardsubheader">
            Have ways to improve this site? We welcome all who wish to help
            contribute!
          </span>
        </p>
        <a href="/about">
          <v-card color="#4738AC" class="learn">
            <h5>
              <span class="learnheader">Learn more about the Project</span>
            </h5>
          </v-card>
        </a>
      </v-card>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  name: 'TitleBar',
  props: {
    header: {
      type: String,
      default: ''
    },
    titleId: {
      type: Number,
      default: null
    },
    subheader: {
      type: String,
      default: ''
    }
  }
}
</script>
<style lang="scss">
.TitleBar {
  .Background-Wrapper {
    background: url('../static/titlebar_bg.png') center no-repeat;
    height: 340px;
    position: relative;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-bottom: 30px;
    box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25), 0px 4px 4px rgba(0, 0, 0, 0.25);
    @include lessThan($small) {
      display: none;
    }

    .header-container {
      width: 650px;
      height: 75px;
      margin-right: 139px;
      margin-top: 88px;
      margin-bottom: 177px;
      display: flex;
      flex-direction: column;
      padding: 4px 15px;
    }

    .headertitle {
      font-style: normal;
      font-weight: bold;
      font-size: 36px;
      line-height: 49px;
      letter-spacing: 0.03em;
      color: white;
    }

    .headersubtitle {
      font-style: normal;
      font-weight: normal;
      font-size: 16px;
      line-height: 140%;
      color: white;
    }

    //card inside card
    .card {
      width: 472px;
      height: 190px;
      box-shadow: 0px 3px 5px rgba(0, 0, 0, 0.25),
        0px 0px 3px rgba(0, 0, 0, 0.1);
      @media screen and (max-width: 1150px) {
        display: none;
      }
      //Help us raise bay area...

      .cardheader {
        position: absolute;
        left: 24px;
        right: 24px;
        top: 26px;
        height: 27px;
        width: 100%;
        font-style: normal;
        font-weight: bold;
        font-size: 18px;
        line-height: 27px;
        justify-content: center;
        align-items: center;
      }

      //Have ways to improve...
      .cardsubheader {
        position: absolute;
        height: 40px;
        left: 24px;
        top: 30px;
        bottom: 90px;
        font-style: normal;
        font-weight: normal;
        font-size: 14px;
        line-height: 140%;
        margin-top: 30px;
      }

      //card for learn more about project
      .learn {
        position: absolute;
        width: 268px;
        height: 50px;
        right: 24px;
        bottom: 20px;
        border-radius: 5px;

        //learn more about the project
        .learnheader {
          position: absolute;
          width: 225px;
          height: 22px;
          top: 16px;
          right: 21px;
          bottom: 12px;
          left: 22px;
          font-style: normal;
          font-weight: bold;
          font-size: 13.5px;
          line-height: 22px;
          text-align: center;
          color: white;
        }
      }
    }
  }
}
</style>
