<template>
  <div>
    <div class="row">
      <h1 class="heading">text</h1>
      <AtomInputText v-model="textValue" />
      <p>値：{{ textValue }}</p>
    </div>
    <div class="row">
      <h1 class="heading">textarea</h1>
      <AtomTextArea v-model="textAreaValue" />
      <p>値：{{ textAreaValue }}</p>
    </div>
    <div class="row">
      <h1 class="heading">select</h1>
      <AtomSelect v-model="selectValue" :options="options" />
      <p>値：{{ selectValue }}</p>
    </div>
    <div class="row">
      <h1 class="heading">radio</h1>
      <AtomRadios v-model="radioValue" :options="options" />
      <p>値：{{ radioValue }}</p>
    </div>
    <div class="row">
      <h1 class="heading">checkbox（単数）</h1>
      <AtomCheckbox v-model="singleCheckboxValue" label="チェックする" />
      <p>値：{{ singleCheckboxValue }}</p>
    </div>
    <div class="row">
      <h1 class="heading">checkbox（複数）</h1>
      <label>
        <input v-model="checkboxValue" type="checkbox" value="選択肢1" />
        選択肢1
      </label>
      <label>
        <input v-model="checkboxValue" type="checkbox" value="選択肢2" />
        選択肢2
      </label>
      <label>
        <input v-model="checkboxValue" type="checkbox" value="選択肢3" />
        選択肢3
      </label>
      <p>値：{{ checkboxValue }}</p>
    </div>
  </div>
</template>

<script lang="ts">
import AtomInputText from '~/components/atoms/AtomInputText.vue'
import AtomTextArea from '~/components/atoms/AtomTextArea.vue'
import AtomSelect from '~/components/atoms/AtomSelect.vue'
import AtomRadios from '~/components/atoms/AtomRadios.vue'
import AtomCheckbox from '~/components/atoms/AtomCheckbox.vue'

export default {
  components: {
    AtomInputText,
    AtomTextArea,
    AtomSelect,
    AtomRadios,
    AtomCheckbox
  },
  data() {
    return {
      textValue: '',
      textAreaValue: '',
      selectValue: '',
      radioValue: '',
      singleCheckboxValue: false,
      checkboxValue: [],
      options: ['選択肢1', '選択肢2', '選択肢3']
    }
  }
}
</script>

<style scoped>
.row {
  margin-bottom: 10px;
}
.heading {
  font-size: 20px;
  margin-bottom: 10px;
}
</style>
