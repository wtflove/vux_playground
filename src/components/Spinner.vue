<template>
  <div>
    <!-- <atom-spinner :animation-duration="1000" :size="60" :color="'#ff1d5e'"></atom-spinner> -->
    <loading-spinner class="spinner"></loading-spinner>
    <!-- <atom-spinner :animation-duration="1000" :size="60" :color="'#ff1d5e'"></atom-spinner> -->
    <!-- <p>Loading Spinner is above!</p> -->
  </div>
</template>
<script>
/* eslint-disable */
import { AtomSpinner } from 'epic-spinners'
import LoadingSpinner from './LoadingSpinner.vue'

export default {
  name: 'Spinner',
  components: {
    AtomSpinner,
    LoadingSpinner
  }
}

</script>
<style>
body,
html {
  height: 100%;
  width: 100%;
}

.spinner {
  position: absolute;
  display: block;
  /*margin: auto;*/
  /*vertical-align: middle;*/
  /*margin-right: auto;*/
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

</style>
