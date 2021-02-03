<template>
  <div>
    <div>C组件</div>
    <slot name="c" />
    <div v-for="item in data" :key="item.id">
      <div v-if="!item.children">{{ item.id }}</div>
      <div v-else>
        <cw :data="item.children">
          <!-- <template slot="c"> 123 </template> -->
          <template v-for="slotName in Object.keys($scopedSlots)" :slot="slotName">
            <slot :name="slotName"></slot>
          </template>
        </cw>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'cw',
  mounted() {
    console.log(this.$scopedSlots)
  },
  props: {
    data: {
      type: Array,
      default() {
        return []
      }
    }
  },
  data() {
    return {}
  }
}
</script>
<style scoped></style>
