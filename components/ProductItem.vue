<template>
  <div class="card text-white bg-dark mb-3" style="width: 18rem">
    <div class="card-body">
      <h5 class="card-title">{{ nom }}</h5>
      <h6 class="card-subtitle mb-2 text-muted">Prix : {{ prix }}€</h6>
      <p class="card-text" v-if="role == 'commander'">This is food.</p>
      <a href="#" class="card-link" v-if="role == 'commander'"
        >Buy some {{ nom }}</a
      >
      <hr v-if="role == 'commander'" />
      <button
        v-if="role == 'commander'"
        @click="$emit('commande', nom, prix)"
        class="btn btn-success"
      >
        Commander
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProductItem",
  props: ["nom", "prix", "role"],
};
</script>
