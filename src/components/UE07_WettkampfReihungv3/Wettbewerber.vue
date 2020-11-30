<template>
  <div id="padder">
    <div id="name">{{ competitor }}</div>
    <div id="sentence">{{ ranking }}</div>
    <div>
      <md-radio v-for="(element, index) in taken" :key="index" v-model="radio" :disabled=element
                :value="index"
                @change="onSelectDifferentRadio(index)">{{ index + 1 }}
      </md-radio>
    </div>
  </div>
</template>

<script>
import eventBus from '@/services/event-bus'

export default {
  name: "Wettbewerber",
  props: {
    competitor: String,
    taken: Array
  },
  data() {
    return {
      taken: [],
      ranking: "",
      radio: null,
      last: null
    }
  },
  methods: {
    onSelectDifferentRadio(rank) {
      this.taken[rank] = true
      this.ranking = rank + 1 + ". Platz"
      eventBus.$emit("onSelect", [rank, this.last])
      this.last = rank
    },
    updateButtons(input) {
      if (input[1] !== undefined)
        eventBus.$set(this.taken, input[1], false);
      eventBus.$set(this.taken, input[0], true);
    }
  },
  created() {
    this.taken = new Array(this.taken.length).fill(false)
    eventBus.$on("onSelect", (data) => {
          this.updateButtons(data)
        }
    )
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
  width: 12em;
}

#sentence {
  margin-top: 15px;
  width: 8em;
}
</style>