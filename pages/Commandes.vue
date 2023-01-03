<template>
  <div>
    <h1>Passer commande</h1>
    <h2>Produits disponibles :</h2>
    <div class="card-group">
      <ProductItem
        v-for="product in products"
        v-bind:key="product.key"
        v-bind:nom="product.name"
        v-bind:prix="product.price"
        v-on:commande="ajouterProduit"
        role="commander"
      />
    </div>
    <div class="card-group">
      <ProductItem
        v-for="product in commandes"
        v-bind:key="product.key"
        v-bind:nom="product.name"
        v-bind:prix="product.price"
        role="afficher"
      />
    </div>
  </div>
</template>

<script>
import ProductItem from "../components/ProductItem.vue";
export default {
  name: "commandes",
  components: ProductItem,
  data() {
    return {
      products: [
        { key: 1, name: "Pizza", price: 5.0 },
        { key: 2, name: "Tacos", price: 5 },
        { key: 3, name: "Burger", price: 4.0 },
        { key: 4, name: "Frites", price: 2.5 },
      ],
      commandes: [{ key: 4, name: "Frites", price: 2.5 }],
    };
  },
  methods: {
    ajouterProduit(nom, prix) {
      this.commandes.push({ name: nom, price: prix });
    },
  },
};
</script>

<style></style>
