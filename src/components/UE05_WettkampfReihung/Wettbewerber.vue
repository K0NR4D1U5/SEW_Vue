<!--<template>-->
<!--  <div id="padder">-->
<!--    <div id="name">{{ competitor }}</div>-->
<!--    <div id="sentence">{{ ranking }}</div>-->
<!--    <div>-->
<!--      <md-radio v-model="radio" value="1" @change="onSelectDifferenRadio(1)" :disabled=taken[0]>1</md-radio>-->
<!--      <md-radio v-model="radio" value="2" @change="onSelectDifferenRadio(2)" :disabled=taken[1]>2</md-radio>-->
<!--      <md-radio v-model="radio" value="3" @change="onSelectDifferenRadio(3)" :disabled=taken[2]>3</md-radio>-->
<!--      <md-radio v-model="radio" value="4" @change="onSelectDifferenRadio(4)" :disabled=taken[3]>4</md-radio>-->
<!--      <md-radio v-model="radio" value="5" @change="onSelectDifferenRadio(5)" :disabled=taken[4]>5</md-radio>-->
<!--    </div>-->
<!--  </div>-->
<!--</template>-->

<!--<script>-->
<!--export default {-->
<!--  name: "Wettbewerber",-->
<!--  props: {-->
<!--    competitor: String,-->
<!--    taken: Array-->
<!--  },-->
<!--  data() {-->
<!--    return {-->
<!--      ranking: "",-->
<!--      radio: null,-->
<!--      last: null-->
<!--    }-->
<!--  },-->
<!--  methods: {-->
<!--    onSelectDifferenRadio(rank) {-->
<!--      this.taken[rank - 1] = true;-->
<!--      this.ranking = rank + ". Platz";-->
<!--      this.$emit("onSelect", [rank,this.last]);-->
<!--      this.last = rank;-->
<!--    }-->
<!--  }-->
<!--}-->
<!--</script>-->

<!--<style scoped>-->
<!--#padder {-->
<!--  padding: 10px;-->
<!--  margin: 10px;-->
<!--  display: flex;-->
<!--  flex-direction: row;-->
<!--  justify-content: space-between;-->
<!--}-->

<!--#name {-->
<!--  margin-top: 15px;-->
<!--  font-weight: bold;-->
<!--  width: 10em;-->
<!--}-->

<!--#sentence {-->
<!--  margin-top: 15px;-->
<!--  width: 15em;-->
<!--}-->
<!--</style>-->