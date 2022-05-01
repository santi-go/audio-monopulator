<template>
  <div>
    <h1>Sandbox</h1>
    <button @click="playNote">C4</button>
  </div>
</template>

<script lang="ts">
  import Vue from 'vue'
  import * as Tone from 'tone'

  const synth = new Tone.Synth().toDestination();

  export default Vue.extend({
    name: 'Sandbox',
    methods: {
      playNote(): void {
        synth.triggerAttackRelease("C4", "8n");
      }
    }
  })
</script>

<style scoped>

</style>