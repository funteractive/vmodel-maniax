<template>
  <input type="text" :value="value" @input="inputHandler" />
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'AtomInputText',
  props: {
    value: { type: String, required: true }
  },
  methods: {
    inputHandler(e: any): void {
      this.$emit('input', e.target.value)
    }
  }
})
</script>

<style scoped lang="scss"></style>
