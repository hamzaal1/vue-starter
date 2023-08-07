<template lang="">
    <div>
        <h3>Calcul</h3>
        Enter Number 1 <input type="text"   @input="event => input1 = Number(event.target.value)" :value="input1">
        Enter Number 2 <input type="text"   @input="event => input2 = Number(event.target.value)" :value="input2"> <br>
        <button @click="sum()">+</button>
        <button @click="division()">/</button>
        <button @click="sub()">-</button>
        <button @click="asterisk()">*</button>
        <p>Result : {{ result }}</p>
    </div>
</template>
<script setup>
import { ref } from 'vue'
const result = ref(0)
const input1 = ref(0)
const input2 = ref(0)

function sum() {
  result.value = input1.value + input2.value
  input1.value = 0
  input2.value = 0
}

function division() {
  if (input2 !== 0) {
    result.value = input1.value / input2.value
    input1.value = 0
    input2.value = 0
  }else{
    result.value = 0
  }
}

function sub() {
  result.value = input1.value - input2.value
  input1.value = 0
  input2.value = 0
}

function asterisk() {
  result.value = input1.value * input2.value
  input1.value = 0
  input2.value = 0
}
</script>
<style lang="">
</style>