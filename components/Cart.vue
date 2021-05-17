<template>
  <div class="ec-cart-widget"></div>
</template>

<script>
  function injectCartScript(storeId) {
    const cartScript = document.createElement("script");

    cartScript.setAttribute("type", "text/javascript");
    cartScript.setAttribute("charset", "utf-8");
    cartScript.setAttribute("data-cfasync", "false");
    cartScript.setAttribute(
    "src",
    `https://app.ecwid.com/script.js?${storeId}&data_platform=code&data_date=2021-05-17`
    );
    cartScript.onload = injectEcwidInit(storeId);
    document.head.appendChild(cartScript);
  }
  function injectEcwidInit(storeId) {
    return function () {
      const ecwidInitScript = document.createElement("script");

      ecwidInitScript.setAttribute("type", "text/javascript");
      ecwidInitScript.setAttribute("charset", "utf-8");
      ecwidInitScript.text = `Ecwid.init();`;
      document.head.appendChild(ecwidInitScript);
    }
  }
export default {
    name: "Cart",
    props: {
      storeId: {
      type: Number,
      default: 60974400
      }
    },

    mounted() {
      injectCartScript(this.storeId);
    }
}
</script>