<template>
  <div>
    <label v-for="option in options" :key="option">
      <input
        v-model="value"
        type="radio"
        :value="option"
        @input="inputHandler"
      />
      {{ option }}
    </label>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'AtomRadios',
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
