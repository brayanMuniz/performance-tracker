<template>
  <div id="app">
    <h1>Performance Tracker</h1>

    <div class="flex-container">
      <button v-for="btn in amountOfButtons" :key="btn" style="margin: 10px">
        Bunch of buttons
      </button>
    </div>

    <div class="flex-container">
      <div style="margin: 10px">Code Here</div>
      <div style="margin: 10px">Chart showing data Here</div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component({
  components: {},
})
export default class App extends Vue {
  amountOfButtons = 5;
}
</script>

<style>
.flex-container {
  display: flex;
  flex-wrap: wrap;
}
</style>

