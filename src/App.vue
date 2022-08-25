<script setup>
import { ref } from "vue";
const valor1 = ref("");
const valor2 = ref("");
</script>
<template>
  <main>
    <h2>Calculadora de Gorjetas</h2>

    <label>Qual o valor da conta?</label>
    <input type="number" v-model="valor2" />
    <label>Como foi o Serviço?</label>
    <select name="Qualidade do serviço" v-model="gorjeta" id="asd">
      <option value="5">5% (Péssimo)</option>
      <option value="10">10% (Ruim)</option>
      <option value="15">15% (Ok)</option>
      <option value="20">20% (Bom)</option>
      <option value="25">25% (muito Bom)</option>
      <option value="30">30% (Perfeito)</option>
    </select>
    <label>Quantas pessoas estão pagando a conta?</label>
    <input type="number" v-model="valor1" />
    <h3>
      Valor para cada um pagar: R${{ (valor1 * (1 + gorjeta / 100)) / valor2 }}
    </h3>
  </main>
</template>
<style>
input {
  display: block;
  width: 250px;
  height: 25px;
  margin-bottom: 15px;
  border: 1px solid rgb(255, 255, 255);
  border-radius: 10px;
}
h2 {
  background-color: rgb(171, 194, 180);
  height: 40px;
  padding: 3px;
  color: rgb(255, 255, 255);
  border-radius: 10px;
  text-align: center;
}
select {
  display: block;
  width: 250px;
  height: 25px;
  margin-bottom: 15px;
  border: 1px solid black;
  border-radius: 10px;
}

main {
  background-color: rgb(209, 209, 209);
  padding: 30px;
  margin: 50% auto;
  border-radius: 8px;
  margin-left: 45%;
  height: 300px;
  width: 500px;
}
</style>
