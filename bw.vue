<template>
  <div>
    <div>B组件</div>
    <cw :data="data">
      <template slot="c">
        <slot name="b" />
      </template>
    </cw>
  </div>
</template>

<script>
import cw from './cw.vue'
export default {
  components: {
    cw
  },
  data() {
    return {
      data: [
        {
          id: 2,
          children: [
            {
              id: 21,
              children: [{ id: 211 }, { id: 212 }]
            }
          ]
        }
      ]
    }
  }
}
</script>
<style scoped></style>
