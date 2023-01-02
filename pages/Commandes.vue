<template>
  <div>
    <h1>Passer commande</h1>
    <h2>Produits disponibles :</h2>
    <div
      v-for="product in products"
      :key="product.key"
      class="card text-white bg-dark mb-3"
      style="width: 18rem"
    >
      <div class="card-body">
        <h5 class="card-title">{{ product.name }}</h5>
        <h6 class="card-subtitle mb-2 text-muted">
          Prix : {{ product.price }}€
        </h6>
        <p class="card-text">This is food.</p>
        <a href="#" class="card-link">Buy some {{ product.name }}</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "commandes",
  data() {
    return {
      products: [
        { key: 1, name: "Pizza", price: 5.0 },
        { key: 2, name: "Tacos", price: 5 },
        { key: 3, name: "Burger", price: 4.0 },
        { key: 4, name: "Frites", price: 2.5 },
      ],
    };
  },
};
</script>

<style></style>
