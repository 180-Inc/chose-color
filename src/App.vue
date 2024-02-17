<template>
  <div>
    <h1>色の画像を表示するアプリ</h1>
    <p>好きな色を選んでください。</p>
    <input type="checkbox" id="red" value="red" v-model="colors">
    <label for="red">レッド</label>
    <input type="checkbox" id="blue" value="blue" v-model="colors">
    <label for="blue">ブルー</label>
    <input type="checkbox" id="purple" value="purple" v-model="colors">
    <label for="purple">パープル</label>

    <p>選択した色は{{ colors }}</p>
    <div v-for="color in colors" :key="color">
      <div :style="{backgroundColor: color}" class="displayColor"></div>
    </div>
  </div>
</template>

<!-- Option API -->
<!-- <script>
export default {
  data() {
    return {
      colors: [],
    };
  },
}
</script> -->

<script setup>
import { ref } from 'vue';

const colors = ref([]);

</script>

<style>
  .displayColor {
    width: 300px;
    height: 300px;
  }
</style>

