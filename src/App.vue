<template>
  <div id="app">
    <inventory-header
      :authenticated="authenticated"
      @login="authenticated = true"
      @logout="authenticated = false"
    />
    <product-inventory :authenticated="authenticated" />
  </div>
</template>

<script>
import InventoryHeader from "./components/InventoryHeader.vue";
import ProductInventory from "./components/ProductInventory.vue";

export default {
  name: "App",
  components: {
    ProductInventory,
    InventoryHeader,
  },
  data() {
    return {
      authenticated: false,
    };
  },
};
</script>

<style>
body {
  background-color: rgb(178, 194, 192);
  margin: 0;
  padding-bottom: 50px;
}

#app {
  font-family: Helvetica, Arial, sans-serif;
}
</style>
