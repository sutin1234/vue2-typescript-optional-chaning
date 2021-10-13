<template>
  <div>
    <h1>Test</h1>
    <HelloWorld :msg="msg" :address="address" />
  </div>
</template>

<script lang="ts">
import HelloWorld from '@/components/HelloWorld.vue'
import { Vue, Component } from 'vue-property-decorator'
@Component({
  components: {
    HelloWorld: HelloWorld
  }
})
export default class Test extends Vue {
  msg = 'Hello Vue2 Typescript'
  address = {
    locaytions: {},
    city: 'BKK'
  }
}
</script>

<style scoped>
div {
  padding: 20px;
}
</style>
