<template>
  <select @input="inputHandler">
    <option v-for="option in options" :key="option">{{ option }}</option>
  </select>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'AtomSelect',
  props: {
    options: { type: Array, required: true },
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
