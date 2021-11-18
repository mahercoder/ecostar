<template>
  <div class="map" id="con">
    <v-container class="py-none">
      <v-row>
        <v-col cols="12" lg="5" md="6" sm="8" class="contact">
          <contact />
        </v-col>
      </v-row>
    </v-container>
    <iframe class="iframe" src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d6067.391608615423!2d70.93307314813232!3d40.504109273853096!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zNDDCsDMwJzE2LjgiTiA3MMKwNTYnMDYuNiJF!5e0!3m2!1sru!2s!4v1613130766660!5m2!1sru!2s" width="100%" height="450" frameborder="0" style="border:0;" allowfullscreen="" aria-hidden="false" tabindex="0"></iframe>
    <iframe class="iframe_sm" src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d6067.391608615423!2d70.93307314813232!3d40.504109273853096!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zNDDCsDMwJzE2LjgiTiA3MMKwNTYnMDYuNiJF!5e0!3m2!1sru!2s!4v1613130766660!5m2!1sru!2s" width="100%" height="450" frameborder="0" style="border:0;" allowfullscreen="" aria-hidden="false" tabindex="0"></iframe>
  </div>
</template>
<script>
import contact from "./contact";
export default {
  components: {
    contact,
  },
};
</script>
<style lang="scss" scoped>
.map{
  position: relative;
  .iframe{
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    width: 100%;
    z-index: 1;
  }
  .contact{
    position: relative;
    z-index: 3;
     padding-bottom: 0px !important;
  }
  .py-none{
    padding-bottom: 0px !important;
  }
  .iframe_sm{
    display: none;
  }
  @media (max-width:599px) {
    .iframe{
      display: none;
    }
    .iframe_sm{
      display: block;
    }
  }
}
</style>
