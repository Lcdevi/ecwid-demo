<template>
  <div id="shop">
    <div id="app">
      <Ecwid :storeId="60974400"/>
    </div>
  </div>
  <!--START SERVICES-->
  <!-- <section class="section pt-5" id="services">
    <div class="container">
      <div class="row">
        <div class="col-lg-8 offset-lg-2">
          <h1 class="section-title text-center">SHOP</h1>
            <div id="app">
              <Ecwid :storeId="60974400"/>
            </div>
            
          <div class="section-title-border margin-t-20"></div>
        </div>
      </div>
    </div>
  </section> -->
  <!--START SERVICES-->
</template>

<script>
  import Ecwid from "~/components/Ecwid.vue";

  export default {
    name: "App",
      components: {
        Ecwid
      }
  };
</script>

<style scoped>
#shop {
  color: #6e6e63;
  padding: 120px 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: #fcfbfa;
}
#app {
  margin: 120px;
  background-color: #fcfbfa;
}
</style>