<template>
  <div>
    <label>
      <input v-model="value" type="checkbox" @input="inputHandler" />
      {{ label }}
    </label>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'AtomCheckbox',
  props: {
    label: { type: String, default: '' },
    value: { type: Boolean, required: true }
  },
  methods: {
    inputHandler(e: any): void {
      this.$emit('input', e.target.checked)
    }
  }
})
</script>

<style scoped lang="scss"></style>
