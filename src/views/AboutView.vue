<script setup>
import { useRouter } from 'vue-router'

const router = useRouter()

const goBackHome = () => {
  router.push({ name: 'home' })
}
</script>

<template>
  <div class="about">
    <h2>Пока вы можете только отправить мне USDT(TRC 20) на этот адрес:</h2>
    <img src="../assets/usdt.png" alt="QRcode" class="qr" />
    <span class="address">TUa3GHF7V1TEAX2RfW8poLjdB4CyxuTfRn</span>
    <button @click="goBackHome" class="button">Вернуться назад</button>
  </div>
</template>

<style>
.about {
  background-color: #000;
  color: #ffd700; /* Золотой цвет */
  font-family: 'Arial', sans-serif;
  text-align: center;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}
.qr {
  margin: 30px 0;
}

.address {
  font-size: 12px;
}

.button {
  background: linear-gradient(
    145deg,
    #ffcc00,
    #b8860b
  ); /* Градиент от светло золотого к темно золотому */
  color: #000;
  font-size: 1rem;
  font-weight: bold; /* Сделано более жирным */
  padding: 15px 30px;
  width: 200px;
  margin: 20px auto;
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
