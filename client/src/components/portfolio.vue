<template>
  <section id="port">
    <v-container>
      <h1>Sizga quyidagi xizmatlarni taklif qilamiz</h1>
      <v-row>
        <v-col cols="12" lg="3" md="4" sm="6" v-for="(n,i) in item" :key="n.img" >
          <div class="wrapper" @mouseover="hoverOverlay(i, $event)">
            <img :src="n.img" alt="" />
            <div ref="overlay" class="overlay"></div>
            <v-btn class="btn_gradient" tag="a" href="https://t.me/Ecostaruz2">
              Buyurtma berish
            </v-btn>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>
<script>
export default {
  data: () => ({
    item: [
      {
        img: require("../assets/1.jpg"),
      },
      {
        img: require("../assets/2.2.jpg"),
      },
      {
        img: require("../assets/3.jpg"),
      },
      {
        img: require("../assets/4.jpg"),
      },
      {
        img: require("../assets/5.jpg"),
      },
      {
        img: require("../assets/Group 138.jpg"),
      },
      {
        img: require("../assets/7.jpg"),
      },
      {
        img: require("../assets/8.jpg"),
      },
    ],
  }),
  methods:{
    // hoverOverlay(i,e){
    //   // const overlay = document.querySelectorAll('.wrapper .overlay')
    //   this.$refs.overlay[i].style.clipPath = `circle(200% at ${e.clientY}px ${e.clientX}px)`;
    //   console.log(e,i);
    // }
  }
};
</script>
<style lang="scss" scoped>
section{
  padding:90px 0;
}
h1 {
  font-family: 'Open Sans';
  font-style: normal;
  font-weight: bold;
  font-size: 36px;
  line-height: 150%;
  text-align: center;
  color: #454545;
  margin-bottom: 60px;
}
img {
  width: 100%;
  height: 100%;
}
.wrapper{
  position: relative;
  overflow: hidden;
  .btn_gradient {
    bottom: 0;
    left: 0;
    position: absolute;
    background: linear-gradient(85.45deg, #0cab1e 0%, #62d61b 100%);
    border-radius: 15px;
    color: white;
    font-size: 18px;
    padding: 17px 0px !important;
    width: 100%;
    height: 60px !important;
    transform: translateY(80px);
    z-index: 2;
  }
  .overlay{
    background: rgba($color: #000000, $alpha: 0.3);
    backdrop-filter: blur(2px);
    position: absolute;
    border-radius: 15px;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    width: 100%;
    height: calc(100% - 5px);
    z-index: 1;
    clip-path: circle(0% at 83% 80%);
    transition: 0.5s;
  }
  &:hover .overlay{
    clip-path: circle(200% at 83% 55%);
  }
  &:hover .btn_gradient{
    transform: translateY(0px);
  }
}
</style>