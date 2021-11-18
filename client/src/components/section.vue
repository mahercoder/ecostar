<template>
  <section class="skill">
    <v-container>
      <v-row>
        <v-col cols="12" md="6">
          <img src="../assets/about_left.png" alt="" />
        </v-col>
        <v-col cols="12" md="6">
          <h1>Xohlangan turdagi mahsulotlarni qadoqlash xizmati</h1>
          <p>
            Darhol biz bilan bog’laning va o'z mahsulotingiz uchun chiroyli,
            zamonaviy dizayn va upakovkaga ega bo'ling.
          </p>
          <v-btn class="btn_gradient" tag="a" href="https://t.me/Ecostaruz2"> Buyurtma berish </v-btn>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>
<script>
export default {};
</script>
<style lang="scss" scoped>
.skill {
  padding: 85px 0;
}
img {
  max-width: 100%;
  height: auto;
}
h1 {
  font-family: "Open Sans";
  font-style: normal;
  font-weight: bold;
  font-size: 28px;
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
@media (max-width:699px) {
  .skill{
    text-align: center;
  }
}
</style>
