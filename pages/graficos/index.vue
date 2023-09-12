<style>
.TodosGraficos{
  display: grid;
  grid-template-columns: repeat(1, 1fr);
  justify-content: center;
  align-items: center;
  max-width: 100%;
  max-height: 100%;
  margin: 20px;
  padding: 5px; 
  gap: 10px;
}

.PrimeiroGrafico{
  max-width: 100%; 
  height: 100%;
  padding: 10px;
  margin-bottom: 20px; 
}

.SegundoGrafico{
  max-width: 100%; 
  height: 100%;
  padding: 10px;
  margin-bottom: 20px; 
}

.TerceiroGrafico{
  max-width: 100%; 
  height: 100%;
  padding: 10px;
  margin-bottom: 20px; 
}

</style>


<template>
  <div class="inicioInvestidor">
    <h2>SIIIA | GRÁFICOS DE ANÁLISE</h2>
    <p> Sistema Integrado de Investimento e Inclusão Agrária</p>
  </div>

  <div class="inicioInvestidor">
    <div class="sia-card-1">
      <table>
        <tr>
          <td rowspan="2">
            <div class="icon-notf2"></div>
          </td>
          <td style="vertical-align: bottom;">
            <h2 class="title h2Solicitacao">Monitoramento de preços e tendências de mercado</h2>
          </td>
        </tr>
        <tr>
          <td style="vertical-align: top;">
            <p class="desc pInvista">Acompanhamento da evolução dos preços dos produtos agrícolas disponíveis no mercado...</p>
          </td>
        </tr>
      </table>
    </div>
  </div>


  <div class="TodosGraficos">
    <div class="PrimeiroGrafico">
      <ModalPrimeiroGrafico />
    </div>
    <div class="SegundoGrafico">
      <ModalSegundoGrafico />
    </div>
    <div class="TerceiroGrafico">
      <ModalTerceiroGrafico />
    </div>
  </div>


</template> 