<template>
  <div>
    <div class="row">
      <h1 class="heading">text</h1>
      <input v-model="textValue" type="text" />
      <p>値：{{ textValue }}</p>
    </div>
    <div class="row">
      <h1 class="heading">textarea</h1>
      <textarea v-model="textAreaValue" />
      <p>値：{{ textAreaValue }}</p>
    </div>
    <div class="row">
      <h1 class="heading">select</h1>
      <select v-model="selectValue">
        <option>選択肢1</option>
        <option>選択肢2</option>
        <option>選択肢3</option>
      </select>
      <p>値：{{ selectValue }}</p>
    </div>
    <div class="row">
      <h1 class="heading">radio</h1>
      <label>
        <input v-model="radioValue" type="radio" value="選択肢1" />
        選択肢1
      </label>
      <label>
        <input v-model="radioValue" type="radio" value="選択肢2" />
        選択肢2
      </label>
      <label>
        <input v-model="radioValue" type="radio" value="選択肢3" />
        選択肢3
      </label>
      <p>値：{{ radioValue }}</p>
    </div>
    <div class="row">
      <h1 class="heading">checkbox（単数）</h1>
      <label>
        <input v-model="singleCheckboxValue" type="checkbox" />
        チェックする
      </label>
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
export default {
  data() {
    return {
      textValue: '',
      textAreaValue: '',
      selectValue: '',
      radioValue: [],
      singleCheckboxValue: false,
      checkboxValue: []
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
