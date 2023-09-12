<template>
  <div class="money-container">
    <div v-for="(money, index) in moneyList" :key="index" class="money"
      :style="{ left: money.left + 'px', top: money.top + 'px' }"></div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      moneyList: []
    };
  },
  mounted() {
    this.startMoneyAnimation();
  },
  methods: {
    createMoney() {
      const left = Math.random() * window.innerWidth;
      this.moneyList.push({ left, top: -50 }); // Começa acima da tela
    },
    animateMoney() {
      this.moneyList = this.moneyList.map(money => {
        money.top += 5; // Ajuste a velocidade de queda aqui
        return money;
      });

      // Remova notas de dinheiro que caíram abaixo da tela
      this.moneyList = this.moneyList.filter(money => money.top < window.innerHeight + 50);

      // Agende a próxima animação
      requestAnimationFrame(this.animateMoney);
    },
    startMoneyAnimation() {
      setInterval(() => {
        this.createMoney();
      }, 500); // Cria uma nova nota a cada 500ms

      // Inicia a animação
      requestAnimationFrame(this.animateMoney);
    }
  }
};
</script>

<style scoped>
.money-container {
  position: relative;
  width: 100%;
  height: 100%;
  z-index: 635478;
  overflow: hidden;
}


.money {
  position: absolute;
  width: 280px;
  height: 220px;
  background-image: url('./kwanza.jpeg');
  /* Substitua 'dollar.png' pelo caminho da sua imagem de nota de dinheiro */
  background-size: 80%;
  background-repeat: no-repeat;
  animation: Investimento 3s linear infinite;
}

@keyframes Investimento {
  0% {
    transform: translateY(-30px) rotate(0deg);
    opacity: 0;
  }

  100% {
    transform: translateY(100vh) rotate(160deg);
    opacity: 1;
  }
}</style>
