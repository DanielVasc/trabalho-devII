<script setup>
import { ref } from 'vue'

const SLing = ref([]);
defineProps(["lings"])
</script>

<template>
  <div class="ling">
    <label>Quais as linguagens que voce conhece</label>
    <div v-for="(ling, index) in linguagens" :key="index">
      <input type="checkbox" v-model="SLing" :value="ling.id" :id="ling.id" />
      <label :for="ling.id">{{ ling.name }}</label>
    </div>
    <span> {{ SLing }} </span>
  </div>
</template>

<style>
.ling {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 20px;
  border: 1px solid #3d3b3b;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  background-color: #beb5b5;
  color: #000000;
}
</style>
