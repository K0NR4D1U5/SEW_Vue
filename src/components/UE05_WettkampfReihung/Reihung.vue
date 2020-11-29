<!--<template>-->
<!--  <div class="md-layout">-->
<!--    <md-card class="login-form">-->
<!--      <md-app-toolbar class="md-primary md-dense md-layout md-alignment-center-space-between">-->
<!--        <div class="md-layout-item md-title">-->
<!--          {{ title }}-->
<!--        </div>-->
<!--      </md-app-toolbar>-->
<!--      <div id="padder">-->
<!--        <Wettbewerber competitor="Christoph Schlössl" :taken=taken @onSelect=changeTaken($event)></Wettbewerber>-->
<!--        <Wettbewerber competitor="David Veigel" :taken=taken @onSelect=changeTaken($event)></Wettbewerber>-->
<!--        <Wettbewerber competitor="Patrick Sprengnagl" :taken=taken @onSelect=changeTaken($event)></Wettbewerber>-->
<!--        <Wettbewerber competitor="Konrad Sikorski" :taken=taken @onSelect=changeTaken($event)></Wettbewerber>-->
<!--        <Wettbewerber competitor="Daniel Prokesch" :taken=taken @onSelect=changeTaken($event)></Wettbewerber>-->
<!--      </div>-->
<!--    </md-card>-->
<!--  </div>-->
<!--</template>-->

<!--<script>-->

<!--import Wettbewerber from "@/components/UE05_WettkampfReihung/Wettbewerber";-->

<!--export default {-->
<!--  name: "KonradReihung",-->
<!--  components: {-->
<!--    Wettbewerber-->
<!--  },-->
<!--  props: {-->
<!--    title: String,-->
<!--  },-->
<!--  data() {-->
<!--    return {-->
<!--      taken: [false, false, false, false, false]-->
<!--    }-->
<!--  },-->
<!--  methods: {-->
<!--    changeTaken(rank) {-->
<!--      this.$set(this.taken, rank[0]-1, true);-->
<!--      this.$set(this.taken, rank[1]-1, false);-->
<!--      // this.taken[rank] = true;-->
<!--    }-->
<!--  }-->
<!--}-->
<!--</script>-->

<!--<style scoped>-->
<!--#padder {-->
<!--  padding: 10px;-->
<!--}-->

<!--.login-form {-->
<!--  min-width: 25em;-->
<!--  max-width: 70em;-->
<!--  margin: 10px;-->
<!--}-->
<!--</style>-->