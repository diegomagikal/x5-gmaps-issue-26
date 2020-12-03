<template>
  <q-page class="flex flex-center">

    <div style="width: 700px; height: 70vh">
      <gmaps-map>
        <gmaps-marker :position="position" />
      </gmaps-map>
    </div>

  </q-page>
</template>

<script>

import { x5GMaps, gmapsMarker, gmaps } from 'x5-gmaps'
import Vue from 'vue'

export default {
  components: { 'gmaps-map': gmaps, gmapsMarker },
  mounted () {
    gmaps.then((response) => {
      console.log('response', response)
    })
  },
  data () {
    return {
      position: { lat: -27, lng: 153 }
    }
  }
}
</script>
