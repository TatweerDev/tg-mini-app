<template>
  <div class="about">
    <h2>Пока вы можете только отправить мне USDT(TRC 20) на этот адрес:</h2>
    <img src="../assets/usdt.png" alt="QRcode" class="qr" />
    <span class="address">TUa3GHF7V1TEAX2RfW8poLjdB4CyxuTfRn</span>
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
  /* justify-content: center; */
  /* align-items: center; */
  flex-direction: column;
}
.qr {
  margin: 30px 0;
}

.address {
  font-size: 12px;
}
</style>
