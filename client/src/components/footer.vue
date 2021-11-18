<template>
  <footer>
    <v-container>
      <v-row class="justify-space-between">
        <p>Copyright © {{new Date().getFullYear()}} EcoStar. All rights reserved.</p>
        <p>Developed by <a href="https://cloud9.uz">Cloud9 ITcompany</a></p>
      </v-row>
    </v-container>
  </footer>
</template>
<script>
export default {};
</script>
<style scoped>
footer {
  padding-top: 34px;
  padding-bottom: 34px;
  background: #008809;
}
p{
  margin-bottom: 0px;
  font-family: 'Open Sans';
  font-size: 16px;
  line-height: 22px;
  color: #FFFFFF;
}
a{
  color: #FFFFFF !important;
  font-weight: 600;
  text-decoration: none;
}
@media (max-width:500px) {
  footer{
    text-align: center;
  }
  .justify-space-between{
    justify-content: center !important;
  }
}
</style>
