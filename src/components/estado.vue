<script setup>
import { ref } from 'vue';

let SEst = ref("");
const estados = ref([
      { id: "Acre", name: "AC" },
      { id: "Alagoas", name: "AL" },
      { id: "Amapá", name: "AP" },
      { id: "Amazonas", name: "AM" },
      { id: "Bahia", name: "BA" },
      { id: "Ceará", name: "CE" },
      { id: "Distrito Federal", name: "DF" },
      { id: "Espírito Santo", name: "ES" },
      { id: "Goiás", name: "GO" },
      { id: "Maranhão", name: "MA" },
      { id: "Mato Grosso", name: "MT" },
      { id: "Mato Grosso do Sul", name: "MS" },
      { id: "Minas Gerais", name: "MG" },
      { id: "Pará", name: "PA" },
      { id: "Paraíba", name: "PB" },
      { id: "Paraná", name: "PR" },
      { id: "Pernambuco", name: "PE" },
      { id: "Piauí", name: "PI" },
      { id: "Rio de Janeiro", name: "RJ" },
      { id: "Rio Grande do Norte", name: "RN" },
      { id: "Rio Grande do Sul", name: "RS" },
      { id: "Rondônia", name: "RO" },
      { id: "Roraima", name: "RR" },
      { id: "Santa Catarina ",name: "SC" },
      { id: "São Paulo", name: "SP" },
      { id: "Sergipe", name: "SE" },
      { id: "Tocantins", name: "TO" },
    ]);
</script>

<template>
  <div class="estado">
    <select v-model="SEst">
      <option disabled value="">Selecione o estado</option>
      <option v-for="(estado, index) in estados" :key="index" :value="estado.id">
        {{ estado.name }}
      </option>
    </select>
    <span> {{ SEst }} </span>
  </div>
</template>

<style>
.estado {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 20px;
  border: 1px solid #3f3c3c;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  background-color: #beb5b5;
  color: #000000;
}
</style>