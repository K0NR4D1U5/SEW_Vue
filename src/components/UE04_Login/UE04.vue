<template>
  <md-app
      v-cloak
      md-waterfall
      md-mode="fixed"
  >
    <md-app-toolbar class="md-primary md-dense md-layout md-alignment-center-space-between">
      <router-link to="/">
        <div class="md-layout-item md-title">
          Konrads UE04
        </div>
      </router-link>
    </md-app-toolbar>
    <md-app-content>
      <KonradLogin title="Log in to Fakebook" ph1="E-Mail" ph2="Password" buttonText="Log In"></KonradLogin>
      <KonradLogin title="Log in to Instergram" ph1="Username" ph2="Password" buttonText="Log In"></KonradLogin>
    </md-app-content>
  </md-app>
</template>

<script>
import KonradLogin from "@/components/UE04_Login/Login";

export default {
  name: "UE04",
  components: {
    KonradLogin
  }
}
</script>

<style scoped>
</style>