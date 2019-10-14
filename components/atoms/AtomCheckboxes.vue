<template>
  <div>
    <label v-for="option in options" :key="option">
      <input
        v-model="copiedValue"
        type="checkbox"
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
  name: 'AtomCheckboxes',
  props: {
    options: { type: Array, required: true },
    // value: { type: Array, required: true } as PropOptions<string[]>
    value: { type: Array, required: true }
  },
  data() {
    const copiedValue: string[] = this.value.map((v) => {
      return String(v)
    })
    return {
      copiedValue
    }
  },
  methods: {
    toggleArray(arr: string[], val: string): string[] {
      const copiedArr = arr.slice()
      if (copiedArr.includes(val)) {
        copiedArr.splice(copiedArr.indexOf(val), 1)
      } else {
        copiedArr.push(val)
      }
      return copiedArr
    },
    inputHandler(e: any): void {
      this.$emit('input', this.toggleArray(this.copiedValue, e.target.value))
    }
  }
})
</script>

<style scoped lang="scss"></style>
