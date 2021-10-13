<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      {{ address }}
    </p>
    <p>Locations: {{ address?.locations }}</p>
    <p>Locations: {{ address?.locations ?? 'no locations' }}</p>
    <p>
      Lat, Lng: {{ address?.locations?.lat }}, {{ address?.locations?.lng }}
    </p>
    <p>
      Lat, Lng: {{ address?.locations?.lat ?? 'no Lat' }},
      {{ address?.locations?.lng ?? 'no Lng' }}
    </p>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

interface Location {
  lat: string
  lng: string
}
interface Address {
  locations: Location
  city: string
}
@Component
export default class HelloWorld extends Vue {
  @Prop() msg!: string
  @Prop() address!: Address
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.hello {
  font-size: 20px;
}
</style>
