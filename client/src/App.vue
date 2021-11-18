<template>
  <v-app>
    <v-app-bar app color="white" height="88px" style="z-index: 7; box-shadow:none !important;">
      <div style="width:100%;" class="d-flex align-center">
        <a href="/">
        <img
          alt="star Logo"
          class="shrink mx-8"
          style="flex: 0 0 auto; "
          :src="require('./assets/logo.svg')"
        >
        </a>
        <v-app-bar-nav-icon
          class="toolbar_icon d-block_sm"
          @click.stop="drawer = !drawer"
        ></v-app-bar-nav-icon>
        <v-btn tag="a" class="d-none_720 btnSrc" :href="n.href" v-for="n in buttonLeft" :key="n.name" depressed color="transparent">
          {{ n.name }}
        </v-btn>
      </div>
    </v-app-bar>
    <v-main>
      <v-navigation-drawer v-model="drawer" fixed temporary style="top: 88px; box-shadow:none !important; ">
        <v-list dense>
          <v-list-item v-for="item in buttonLeft" :key="item.name" link class="btnSrc" tag="a" :href="item.href">
            <v-list-item-content>
              <v-list-item-title >{{ item.name }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-navigation-drawer>
      <Header/>
      <About/>
      <Skill/>
      <Portfolio/>
      <Map/>
      <Footer/>
    </v-main>
  </v-app>
</template>

<script>
import Header from './components/header'
import About from './components/about'
import Skill from './components/section'
import Portfolio from './components/portfolio'
import Map from './components/map'
import Footer from './components/footer'
import $ from 'jquery'
const links = ('.btnSrc');

export default {
  name: 'App',

  components: {
    Header,About,Skill,Portfolio,Map,Footer
  },

  data: () => ({
    drawer: false,
    buttonLeft:[
      {
        name:'Biz haqimizda',
        href:"#about"
      },
      {
        name:'Xizmatlarimiz',
        href:"#port"
      },
      {
        name:'Kontaktlarimiz',
        href:"#con"
      },
    ],
  }),
  mounted(){
    $(links).on('click', function (e) {
        e.preventDefault();
        $(links).removeClass('active');
        $(this).addClass('active');
        var id = $(this).attr('href');
        var target = $(id).offset().top - 90;
        $('html, body').animate({
            scrollTop: target,
        }, 1000);
    });
  }
};
</script>
<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;400;600;700;800&display=swap');
.d-block_sm{
  display: none;
}
@media (max-width:720px) {
  .d-none_720{
    display: none;
  }
  .d-block_sm{
  display: block;
}
}
</style>