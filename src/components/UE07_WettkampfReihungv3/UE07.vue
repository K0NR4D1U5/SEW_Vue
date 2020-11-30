<template>
  <md-app
      v-cloak
      md-mode="fixed"
      md-waterfall
  >
    <md-app-toolbar class="md-primary md-dense md-layout md-alignment-center-space-between">
      <router-link to="/">
        <div class="md-layout-item md-title">
          Konrads UE07
        </div>
      </router-link>
    </md-app-toolbar>
    <md-app-content>
      <KonradReihung title="Reihung"></KonradReihung>
    </md-app-content>
  </md-app>
</template>

<script>
import KonradReihung from "@/components/UE07_WettkampfReihungv3/Reihung";

export default {
  name: "UE07",
  components: {
    KonradReihung
  }
}
</script>

<style scoped>
</style>