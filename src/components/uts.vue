<template>
  <div class="container">
    <h1>💖 Hai Noynoy 💖</h1>
    <p>{{ currentMessage }}</p>
    <button @click="generateMessage">ini 😘</button>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const messages = [
  "Kamu alasan aku tersenyum setiap hari 😚",
  "Aku sayang kamu lebih dari kata-kata 💘",
  "Noynoy, kamu segalanya buat aku 💞",
  "Hari-hariku indah karena kamu 🌼",
  "Aku bucin? Iya, dan bangga! 🥰",
  "Cintaku ke kamu nggak ada expired-nya 💯",
  "makasih ya udah selalu ada buat faiq 💓"
]

const currentMessage = ref("Pencet tombol di bawah ya 🥺")

function generateMessage() {
  const randomIndex = Math.floor(Math.random() * messages.length)
  currentMessage.value = messages[randomIndex]
}
</script>

<style scoped>
.container {
  text-align: center;
  padding: 2rem 1rem;
  font-family: 'Comic Sans MS', cursive, sans-serif;
  background: linear-gradient(to right, #ffdde1, #ee9ca7);
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  color: #6b0f1a;
  box-sizing: border-box;
}

h1 {
  font-size: 1.8rem;
  margin-bottom: 1rem;
}

p {
  font-size: 1.2rem;
  margin-bottom: 1.5rem;
  padding: 0 1rem;
}

button {
  padding: 0.8rem 1.2rem;
  font-size: 1rem;
  border: none;
  border-radius: 30px;
  background-color: #ffb6b9;
  color: #fff;
  cursor: pointer;
  transition: background 0.3s;
  width: 100%;
  max-width: 250px;
  margin: 0 auto;
}

button:hover {
  background-color: #fa8e8e;
}
</style>
