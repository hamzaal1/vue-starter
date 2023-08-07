<template>
  <div>
    Hello World from home <br />
    <button @click="decrement">-</button>Count :
    <span :class="{ green: count > 0, red: count < 0 }">{{ count }}</span>
    <button @click="increment">+</button>
    <Hello />
    <ul>
      <li v-for="(item, index) in items" :key="item.id">
        {{ parentMessage }} - {{ index }} - {{ item.message }}
        <button @click="handleDelete(item.id)" class="red">delete</button>
      </li>
    </ul>
    <Calcul />
  </div>
</template>

<script setup>
import { ref } from 'vue'
import Hello from '@/components/WelcomeItem.vue'
import Calcul from '@/components/Calculator.vue'

const count = ref(0)
const items = ref([
  { message: 'Foo', id: 1 },
  { message: 'Bar', id: 2 }
])

function increment() {
  // .value is needed in JavaScript
  count.value++
}
function decrement() {
  // .value is needed in JavaScript
  count.value--
}
function handleDelete(id) {
  // filter array from the element that we want to delete
  items.value = items.value.filter((item) => item.id != id)
}
</script>

<style>
span {
  font-size: 1.3rem;
  margin-inline: 5px;
}
.green {
  color: green;
}
.red {
  color: red;
}
</style>
