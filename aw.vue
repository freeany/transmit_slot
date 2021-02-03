<template>
  <div>
    <div>A组件</div>
    <bw>
      <template slot="b"><slot name="a" /></template>
    </bw>
  </div>
</template>

<script>
import bw from './bw'
export default {
  components: {
    bw
  },
  data() {
    return {}
  }
}
</script>
<style scoped></style>
