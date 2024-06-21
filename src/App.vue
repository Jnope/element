<template>
  <div>
      <el-select v-model="value" multiple placeholder="Select" style="width: 480px">
          <el-option v-for="item in options" :key="item.value" :label="item.label" :value="item.value" />
      </el-select>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

export default defineComponent({
  name: 'App',
  setup() {
      const value = ref([]);
      const options = [
          {
              value: 1,
              label: '前端开发',
          },
          {
              value: 2,
              label: '后端开发',
          },
          {
              value: 3,
              label: '大数据分析',
          },
          {
              value: 4,
              label: 'AI算法工程师',
          },
      ];

      return {
        value,
        options
      }
  },
});
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
