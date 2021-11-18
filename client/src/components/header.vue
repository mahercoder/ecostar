<template>
  <v-container>
    <v-row>
      <v-col cols="12" lg="6">
        <div class="header_title">
          <h1>
            Mahsultongiz uchun ajoyib qadoqlar kerakmi ?
          </h1>
          <p>
            Unda darhol biz bilan bog’laning va o'z mahsulotingiz uchun
            chiroyli, zamonaviy dizayn va upakovkaga ega bo'ling.
          </p>
          <v-btn class="btn_gradient" tag="a" href="https://t.me/Ecostaruz2">
            Buyurtma berish
          </v-btn>
          <div class="header_bottom d-flex justify-space-between align-center">
            <div class="left d-flex align-center">
              <img src="../assets/phone.png" alt="" />
              <a href="tel:+998939712525">+998939712525</a>
            </div>
            <div class="right">
              <a href="https://t.me/Ecostaruz2">
                <img src="../assets/t.svg" alt="" />
              </a>
              <a href="#!">
                <img src="../assets/f.svg" alt="" />
              </a>
              <a href="#!">
                <img src="../assets/i.svg" alt="" />
              </a>
            </div>
          </div>
        </div>
      </v-col>
      <v-col cols="12" lg="6" class="d_none d_block-lg">
        <sliderlg/>
      </v-col>
      <v-col cols="12" lg="6" class="d_block d_none-lg">
        <slider/>
      </v-col>
    </v-row>
  </v-container>
</template>
<script>
import slider from './verticalSlider'
import sliderlg from './sliderlg'

export default {
  components:{
    slider,sliderlg
  }
};
</script>
<style lang="scss" scoped>
.header_title {
  padding-top: 120px;
  padding-bottom: 60px;
  h1 {
    font-family: "Open Sans";
    font-style: normal;
    font-weight: bold;
    font-size: 40px;
    line-height: 130%;
    margin-bottom: 40px;
  }
  p {
    font-family: "Open Sans";
    font-style: normal;
    font-weight: normal;
    font-size: 20px;
    line-height: 150%;
    margin-bottom: 40px;
  }
  .btn_gradient {
    background: linear-gradient(85.45deg, #0cab1e 0%, #62d61b 100%);
    border-radius: 15px;
    color: white;
    font-size: 18px;
    padding: 17px 42px !important;
    height: 60px !important;
    margin-bottom: 120px;
  }
  .header_bottom {
    .left {
      a {
        font-family: "Open Sans";
        font-style: normal;
        font-weight: bold;
        font-size: 20px;
        line-height: 130%;
        color: #5f5f5f;
        margin-left: 20px;
        text-decoration: none;
      }
    }
    .right{
      a{
        margin: 0px 20px;
      }
    }
  }
}
.d_block{
  display: block;
}
.d_none{
  display: none;
}
@media (max-width:1263px) {
  .d_none-lg{
    display: none;
  }
  .d_block-lg{
    display: block;
  }
}
@media (max-width:599px) {
  .header_title{
    text-align: center;
  }
}
@media (max-width:499px) {
  .header_title{
    h1{
      font-size: 25px;
    }
  }
  .header_bottom{
    flex-direction: column;
    justify-content: center !important;
    .right{
      margin-top: 25px;
    }
  }
}
</style>
