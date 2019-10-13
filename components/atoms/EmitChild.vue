<template>
  <button @click.prevent="clickHandler">
    click here!!
  </button>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'EmitChild',
  methods: {
    clickHandler(): void {
      this.$emit('eventName', '引数渡せるよ')
    }
  }
})
</script>

<style scoped lang="scss"></style>
