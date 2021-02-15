<template>
  <md-app
      v-cloak
      md-mode="fixed"
      md-waterfall
  >
    <md-app-toolbar class="md-primary md-dense md-layout md-alignment-center-space-between">
      <router-link to="/">
        <div class="md-layout-item md-title">
          Konrads UE09
        </div>
      </router-link>
    </md-app-toolbar>
    <md-app-content>
      <KonradFormular title="Formular 1"></KonradFormular>
    </md-app-content>
  </md-app>
</template>

<script>
import KonradFormular from "@/components/UE09_FormularMitValidierung/Formular";

export default {
  name: "UE09",
  components: {
    KonradFormular
  }
}
</script>

<style scoped>
</style>
