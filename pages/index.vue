<template>
  <commandes />
  <!-- <Tutorial/> -->
</template>

<script lang="ts">
import Vue from "vue";
import commandes from "./commandes.vue";

export default Vue.extend({
  components: { commandes },
  name: "IndexPage",
});
</script>
