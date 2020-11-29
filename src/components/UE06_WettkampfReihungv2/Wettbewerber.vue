<template>
  <div id="padder">
    <div id="name">{{ competitor }}</div>
    <div id="sentence">{{ ranking }}</div>
    <div>
      <md-radio v-for="(element, index) in taken" v-model="radio" :value="index" :@change="onSelectDifferenRadio(index)"
                :disabled=element>{{index+1}}
      </md-radio>
    </div>
  </div>
</template>

<script>
export default {
  name: "Wettbewerber",
  props: {
    competitor: String,
    taken: Array
  },
  data() {
    return {
      ranking: "",
      radio: null,
      last: null
    }
  },
  methods: {
    onSelectDifferenRadio(rank) {
      this.taken[rank] = true
      this.ranking = rank + 1 + ". Platz"
      this.$emit("onSelect", [rank, this.last])
      this.last = rank
    }
  }
}
</script>

<style scoped>
#padder {
  padding: 10px;
  margin: 10px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

#name {
  margin-top: 15px;
  font-weight: bold;
  width: 10em;
}

#sentence {
  margin-top: 15px;
  width: 15em;
}
</style>