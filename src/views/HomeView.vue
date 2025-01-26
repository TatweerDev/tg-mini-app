<script setup>
import { Alert } from 'vue-tg'
import { ref } from 'vue'
import { useRouter } from 'vue-router'

const balance = ref(0)
const router = useRouter()

const increaseBalance = () => {
  balance.value += 1
}
const goToAbout = () => {
  console.log('Works')
  router.push({ name: 'about' })
}
</script>

<template>
  <main class="main-container">
    <div class="wrapper">
      <h1 class="title">Кнопка Бабло</h1>
      <div class="balance">
        <p>
          У вас на счете: <span class="amount">{{ balance }} $</span>
        </p>
      </div>
      <button class="button" @click="increaseBalance">Бабло</button>
    </div>
    <div>Тут будут курсы криптовалют</div>
    <h3 @click="goToAbout">Вывести Бабло</h3>
    <!-- alerts -->
    <Alert
      ><div>Добро пожаловать!</div>
      <br />
      <div>
        Это приложение - Кнопка бабло. Мечта любого темщика. Кликай на кноку и получай бабло
      </div></Alert
    >
    <Alert
      v-if="balance >= 10"
      message="Поздравляю ты накликал 10$. Продолжай в том же духе и ты станешь миллионером"
    />
  </main>
</template>
<style scoped>
.main-container {
  background-color: #000;
  color: #ffd700; /* Золотой цвет */
  font-family: 'Arial', sans-serif;
  text-align: center;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

.wrapper {
  padding: 20px;
}

.title {
  font-size: 2rem;
  margin-bottom: 20px;
}

.balance {
  font-size: 1.25rem;
  margin-bottom: 30px;
}

.amount {
  font-weight: bold;
}

.button {
  background: linear-gradient(
    145deg,
    #ffcc00,
    #b8860b
  ); /* Градиент от светло золотого к темно золотому */
  color: #000;
  font-size: 1.25rem;
  font-weight: bold; /* Сделано более жирным */
  padding: 15px 30px;
  border: none;
  cursor: pointer;
  border-radius: 5px;
  box-shadow:
    3px 3px 6px #d4af37,
    -3px -3px 6px #d4af37; /* Желтоватое свечение */
  transition: all 0.3s;
}

.button:hover {
  background: linear-gradient(
    145deg,
    #b8860b,
    #ffcc00
  ); /* Инвертированный градиент при наведении */
  box-shadow:
    5px 5px 10px #d4af37,
    -5px -5px 10px #d4af37; /* Более интенсивное свечение при наведении */
}
</style>
