<script setup>
import { ref } from "vue";

const valor2 = ref("");
const valor1 = ref("");
</script>
<template>
  <h2>Calculadora de Gorjetas</h2>
  <h3>Qual o valor da conta?</h3>
  <input type="number" v-model="valor1" placeholder="" />
   <h3>Como foi o serviço?</h3>
  <input type="number" placeholder="" v-model="valor2" />
  <select name="Qualidade de serviço" id="asd" v-model="gorgeta">
    <option value="5">30%</option>
    <option value="10">25%</option>
    <option value="15">20%</option>
    <option value="20">15%</option>
    <option value="25">10%</option>
    <option value="25">5%</option>
  </select>

  <p>Valor para cada um pagar: {{ (valor1 * (1 + gorgeta / 100)) / valor2 }}</p>
</template>
