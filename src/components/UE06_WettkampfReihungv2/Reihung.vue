<template>
  <div class="md-layout">
    <md-card class="login-form">
      <md-app-toolbar class="md-primary md-dense md-layout md-alignment-center-space-between">
        <div class="md-layout-item md-title">
          {{ title }}
        </div>
      </md-app-toolbar>
      <div id="padder">
        <Wettbewerber v-for="competitor in names" :competitor="competitor" :taken="taken"
                      @onSelect=changeTaken($event)></Wettbewerber>
      </div>
    </md-card>
  </div>
</template>

<script>

import Wettbewerber from "@/components/UE06_WettkampfReihungv2/Wettbewerber"
import namesFile from "@/components/UE06_WettkampfReihungv2/names.txt"

export default {
  name: "KonradReihung",
  components: {
    Wettbewerber
  },
  props: {
    title: String,
  },
  data() {
    return {
      taken: [],
      names: []
    }
  },
  created() {
    this.names = namesFile.split("\n")
    this.names.slice(0, (Math.random() * 11) + 5)
    this.taken = new Array(this.names.length)
    this.taken.fill(false)
  },
  methods: {
    changeTaken(rank) {
      this.$set(this.taken, rank[0], true)
      this.$set(this.taken, rank[1], false)
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
  max-width: 70em;
  margin: 10px;
}
</style>