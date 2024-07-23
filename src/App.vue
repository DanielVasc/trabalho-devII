<script setup>
import { ref } from 'vue'
import infos from './components/info.vue';
import estados from './components/estado.vue';
import hobs from './components/hob.vue';
import lings from './components/linguagem.vue';

let bio = ref('')

const Vsenha = () => {
  if (senha.value === Csenha.value) {
    return true
  } 
  
  else {
    alert('As senhas não são iguais')
    return false
  }
}

const enviar = () => {
  if (Vsenha()) {
    const info = {
      nome: nome.value,
      email: email.value,
      nascimento: nascimento.value,
      estado: SEst.value,
      hob: SHob.value,
      linguagens: SLing.value,
      biografia: bio.value
    }
    alert(`Informações: \n${JSON.stringify(info, null, 2)}`)
  }
}
</script>

<template>
  <form @submit.prevent="enviar">
    <p>Escreva sua biografia</p>
    <textarea v-model="bio" />
    <p style="white-space: pre-line"></p>

    <div class="col-12">
      <button class="btn btn-primary" type="submit">Enviar</button>
    </div>
  </form>
</template>

<style>

button[type='submit'] {
  background-color: #4d504d;
  color: #fff;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

button[type='submit']:hover {
  background-color: #676b67;
}
</style>
