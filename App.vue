<template>
  <div>
    <div>App</div>
    <aw>
      <template slot="a">
        <span>slot-a</span>
      </template>
    </aw>
  </div>
</template>

<script>
import aw from './aw'
export default {
  components: {
    aw
  },
  data() {
    return {}
  }
}
</script>
<style scoped></style>
