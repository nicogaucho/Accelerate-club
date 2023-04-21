<script setup>
import { ref } from "vue";

const msg = ref("Player App")
const countPlayer1 = ref(0)
const countPlayer2 = ref(0)

const increment1 = () => countPlayer1.value += 1
const increment2 = () => countPlayer2.value += 1
const decrement1 = () => {
  if (countPlayer1.value > 0) {
    countPlayer1.value -= 1
  } else {
    countPlayer1.value = 0
  }
}
const decrement2 = () => countPlayer2.value -= 1

</script>

<template>
<div class="container">
  <h1>{{ msg }}</h1>
</div>
<div class="grid">
  <article>
    <p>score counter player 1</p>
    <h1>{{ countPlayer1 }}</h1>
    <div class="grid">
      <button @click="increment1()">increment</button>
      <button @click="decrement1()">decrement</button>
    </div>
  </article>
  <article>
    <p>score counter player 2</p>
    <h1>{{ countPlayer2 }}</h1>
    <div class="grid">
      <button @click="increment2()">increment</button>
      <button @click="decrement2()">decrement</button>
    </div>
  </article>
</div>

</template>

<style scoped></style>
