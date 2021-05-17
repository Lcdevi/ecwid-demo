<template>
  <div id="navbar">
    <div class="logo">
      <NuxtLink to="/">
        <img src="~/assets/img/ceucle-logo-transp.png" alt="cèucle logo">
      </NuxtLink>
    </div>
    <div class="links">
      <div class="item itemnav">About</div>
      <a href="/shop" class="itemnav">Shop</a>
      <div class="item itemnav">Contact</div>
      <div id="app" class="itemnav">
        <Cart :storeId="60974400"/>
      </div>
    </div>
  </div>
</template>

<script>
  import Cart from "~/components/Cart.vue";

  export default {
    name: "App",
      components: {
        Cart
      }
  };
</script>

<style scoped>
#navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  height: 110px;
  background-color: #fcfbfa;
}
img {
  max-width: 140px;
  margin: 0 40px;
}
.links {
  display: flex;
  flex-direction: row;
  /* border: 1px solid red; */
  align-items: center;
}
.itemnav {
  margin: 0 40px;
}
</style>