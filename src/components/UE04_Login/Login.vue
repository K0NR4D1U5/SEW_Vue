<template>
  <div class="md-layout">
    <md-card class="login-form">
      <md-app-toolbar class="md-primary md-dense md-layout md-alignment-center-space-between">
        <div class="md-layout-item md-title">
          {{ title }}
        </div>
      </md-app-toolbar>

      <div id="padder">
        <md-field>
          <label>{{ ph1 }}</label>
          <md-input v-model="email" required></md-input>
          <span class="md-error">Please enter an E-Mail.</span>
        </md-field>

        <md-field>
          <label>{{ ph2 }}</label>
          <md-input v-model="passwd" type="password" required></md-input>
          <span class="md-error">Please enter a Password.</span>
        </md-field>

        <md-button class="md-primary md-raised">{{ buttonText }}</md-button>
      </div>
    </md-card>
  </div>
</template>

<script>
export default {
  name: "KonradLogin",
  props: {
    title: String,
    ph1: String,
    ph2: String,
    buttonText: String
  },
  data() {
    return {
      email: null,
      passwd: null
    }
  },
  methods: {
    checkInputs() {

    }
  }

}
</script>

<style scoped>
#padder {
  padding: 10px;
}

.login-form {
  min-width: 25em;
  max-width: 40em;
  margin: 10px;
}
</style>
