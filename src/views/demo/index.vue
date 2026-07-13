<script setup lang="ts">
import { ref } from 'vue';

const count = ref(0);

function handleAdd() {
  count.value += 1;
}
</script>

<template>
  <div class="p-16px">
    <NCard title="Demo 演示" :bordered="false" class="card-wrapper">
      <NSpace vertical :size="16">
        <p class="text-16px">点击下面的按钮，或者在输入框中直接修改数值：</p>
        <NSpace align="center" :size="12">
          <NInputNumber v-model:value="count" placeholder="数值" class="w-200px" />
          <NButton type="primary" @click="handleAdd">点击加 1</NButton>
        </NSpace>
      </NSpace>
    </NCard>
  </div>
</template>

<style scoped></style>
