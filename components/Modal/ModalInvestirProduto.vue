<style>
.BarraModalInvestir {
  background: #0b5ed7;
  color: #fff;
}
.FormularioInvestirProduto {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  width: 100%;
}
.formularioDados input {
  margin: 10px;
  outline: none;
}
.btnFinalizar{
  background: #0b5ed7;
  width: 200px;
  color: #fff;
}
span.saldo{
  color: #09398d;
  font-weight: bold;
}
.saldoDisponivel{
  background: #dddddda1;
  padding: 5px;
  font-size: 1.1rem;
}
span.CSIIA{
  color: green;
}
</style>
 
<template>
  <v-row justify="center">
    <v-dialog v-model="dialog" persistent width="1024">
      <template v-slot:activator="{ props }">
        <v-btn v-bind="props">
          Investir
        </v-btn>

      </template>
      <v-card>
        <v-card-title class="BarraModalInvestir">
          <span class="text-h5 text-white">Investir na Produção</span>
        </v-card-title>
        <v-card-text>
          <v-container>
            <v-row>
              <v-col>

                <div class="saldoDisponivel">
                  <p>Saldo Disponível na sua carteira <span class="CSIIA">SIIA</span></p> <span class="saldo">143.322.020KZ</span>
                </div>

                <div class="FormularioInvestirProduto">
                  <div id="formularioDados">
                    <input class="text-input" type="text" name="nome" placeholder="Capital Solicitado 33.457,00KZ" disabled required>
                    <input class="text-input" type="email" name="email" placeholder="Retorno de 12%" disabled required> 
                  </div>

                  <div id="formularioDados">
                    <input class="text-input" type="text" name="nome" placeholder="8 Meses de Duração" disabled required>
                    <input class="text-input" type="email" name="email" placeholder="Retorno Financeiro de 12.904,000Kz" disabled required>  
                  </div>
                  
                  <div id="formularioDados">
                    <input class="text-input" type="text" name="nome" placeholder="Aplique o valor do investimento" required> 
                  </div>
                </div>

                <div>
                  <p>Ao Finalizar esta operação, o valor de investimento será descontado automaticamente da sua carteira</p>
                </div>
              </v-col>
            </v-row>
          </v-container>
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn color="blue-darken-1" variant="text" @click="dialog = false">
            Fechar
          </v-btn>
          <v-btn color="blue-darken-1" class="btnFinalizar text-white" variant="" @click="dialog = false">
            <p class="text-white">Finalizar</p>
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-row>
</template>
<script>
export default {
  data: () => ({
    dialog: false,
  }),
}
</script>