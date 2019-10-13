<template>
  <EmitChild @eventName="eventNameHandler" />
</template>

<script lang="ts">
import Vue from 'vue'
import EmitChild from '~/components/atoms/EmitChild.vue'

export default Vue.extend({
  name: 'EmitParent',
  components: {
    EmitChild
  },
  methods: {
    eventNameHandler(val: string) {
      // eslint-disable-next-line
      console.log(val)
    }
  }
})
</script>

<style scoped lang="scss"></style>
