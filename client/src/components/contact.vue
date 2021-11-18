<template>
  <div class="card">
    <h3>Kontaktlarimiz</h3>
    <ul class="contact">
      <li>
        <img src="../assets/phones.png" alt="" />
        <div>
          <a href="tel:+998939712525">+998998939712525</a>
        </div>
      </li>
      <li>
        <img src="../assets/loc.png" alt="" />
        <a href="#!">
          Qo’qon shahar <br />
          Burchilik 16-b uy
        </a>
      </li>
      <li>
        <img src="../assets/mess.svg" alt="" />
        <a href="#!">ecostar@gmail.com</a>
      </li>
    </ul>
    <div class="social">
      <ul>
        <li>
          <a href="https://t.me/Ecostaruz2">
            <img src="../assets/tel.svg" alt="" />
          </a>
        </li>
        <li>
          <a href="#!">
            <img src="../assets/face.svg" alt="" />
          </a>
        </li>
        <li>
          <a href="#!">
            <img src="../assets/ins.svg" alt="" />
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>
<script>
export default {
  name: "contact",
};
</script>
<style lang="scss" scoped>
.card {
  background: rgba(248, 248, 248, 0.9);
  backdrop-filter: blur(5px);
  border-radius: 6px;
  padding: 60px;
}
ul {
  margin: 0;
  padding: 0;
  li {
    list-style: none;
    a {
      color: #5f5f5f;
      text-decoration: none;
      margin-left: 20px;
    }
  }
}
h3 {
  font-family: "Open Sans";
  font-style: normal;
  font-weight: bold;
  font-size: 24px;
  line-height: 33px;
  margin-bottom: 40px;
  text-align: center;
}
.contact li {
  display: flex;
  justify-content: flex-start;
  align-items: center;
  list-style: none;
  margin-bottom: 40px;
}
.social {
  ul {
    display: flex;
    justify-content: flex-start;
    align-items: center;
    a {
      margin-left: 0px;
      margin-right: 30px;
    }
  }
}
@media (max-width:400px){
  .card{
    padding-left: 30px;
    padding-right: 30px;
  }
}
</style>
