<script setup>
import { ref } from 'vue'

const SHob = ref([])
defineProps(["hobs"])
</script>

<template>
  <div class="hobs">
    <label>Qual seu hob</label>
    <div v-for="(hob, index) in hobs" :key="index">
      <input type="checkbox" v-model="SHob" :value="hob.id" :id="hob.id" />
      <label :for="hob.id">{{ hob.name }}</label>
    </div>
    <span> {{ SHob }} </span>
  </div>
</template>

<style>
.hobs {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 20px;
  border: 1px solid #555151;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  background-color: #beb5b5;
  color: #000000;
}
</style>
