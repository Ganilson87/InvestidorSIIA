<style scoped>
.FundoDialog {
  background: #dbe1e3;
}

.DetalhesProdutoInvestir {
  display: grid;
  justify-content: center;
  align-items: center;
  margin: 0 auto;
  margin-top: 49px; 
  grid-template-columns: repeat(2, 1fr);
  background: #fff;
  border-radius: 10px;
  padding: 10px;
  width: 1100px;
}

.DetalhesProdutoInvestirFilho1 {
  display: flex;
  flex-direction: column;
  background: url(../../public/img/produtos/cenoura.jpeg);
  background-position: center;
  background-size: 50%;
  background-repeat: no-repeat;
  width: 100%;
  height: 100%;
  border-top-left-radius: 10px;
  border-bottom-left-radius: 10px;
}

.fundoSlogamHistory {
  padding: 20px;
  width: 100%;
  /* backdrop-filter: blur(1px); */
  background: #ffffff41; 
}

p.slogamFazenda {
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 1.5rem;
  color: #fff;
}

span.marcaSlogam {
  color: #031632;
  font-weight: bold;
}

.DetalhesProdutoInvestirFilho2 {
  width: 100%;
  background: #fff;
  border-top-right-radius: 10px;
  border-bottom-right-radius: 10px;
}

.DetalhesProdutoInvestirFilho2 table {
  padding: 20px;
}

.DetalhesProdutoInvestirFilho2 td {
  padding: 5px;
}

.DetalhesProdutoInvestirFilho2 th {
  color: #888888;
  text-align: right;
}

.CapitalPInvestir td,
.CapitalPInvestir th {
  color: #000;
}

.PocicaoTabelasDetalhesProdutosFinanciar {
  margin-top: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 0 auto;
  width: 1100px;
}

/* .btnInvestirProduto{
  background: #0b5ed7;
  width: 100%;
  color: #fff;
  padding: 7px;
  border-radius: 7px;
  cursor: pointer;
  transition: .6s;
} 
.btnInvestirProduto:hover{
  background: #000;
  transition: .6s;
} */



/* Responsividade */

@media(max-width:900px) {
  .DetalhesProdutoInvestir {
    display: grid;
    justify-content: center;
    align-items: center;
    margin: 0 auto;
    margin-top: 49px;
    grid-template-columns: repeat(1, 1fr);
    background: #fff;
    border-radius: 10px;
    padding: 10px;
    width: 100%;
  }

  .SolicitacaoFinanceamento {
    width: 100%;
    margin: 0 auto;
  }

  h2.h2Solicitacao {
    font-size: 1rem;
    padding: 15px;
  }

  p.pInvista {
    font-size: 0.8rem;
    margin-left: 15px;
  }

  .ProdutosDaFazenda {
    /* display: grid;
    grid-template-columns: repeat(2, 1fr); */
    justify-content: center;
    align-items: center;
    margin: 0 auto;
    width: 100%;
    margin: 0 auto;
  }

  @media(max-width:900px) {
    .DetalhesProdutoInvestirFilho1 {
      display: flex;
      justify-content: center;
      align-items: center;
      margin: 0 auto;
      width: 100%;
      height: 100%;
    }
  }

}

@media(max-width:500px) {
  .DetalhesProdutoInvestirFilho2 {
    display: flex;
  }

  p.slogamFazenda {
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 1rem;
    color: #fff;
  }
}


.espacoText{
  margin: 15px;
  text-align: justify;
  font-size: 0.9rem;
}

/* Fim de responsividade */



/* Processo de Producao* /


/** */

.ProcessoProducao{
  display: grid; 
  width: 1135px;  
  margin-left: 130px;
  margin-top: 10px;
  margin-bottom: 30px; 
}
 
</style>

<template>
  <v-row justify="center">
    <v-dialog class="" v-model="dialog" fullscreen :scrim="false" transition="dialog-bottom-transition">
      <template v-slot:activator="{ props }">
        <v-btn class="btnVerFazenda" v-bind="props">
          <p class="text-white">Detalhes</p>
        </v-btn>
      </template>
      <v-card class="FundoDialog">
        <v-toolbar style="background: #0b5ed7;">
          <v-btn icon dark @click="dialog = false">
            <p class="text-white">
              <v-icon icon="home" />
            </p>
          </v-btn>
          <v-toolbar-title class="text-white">
            <p class="text-white">
              Detalhes do Histórico de Produção
            </p>
          </v-toolbar-title>
          <v-spacer></v-spacer>
          <v-toolbar-items class="text-white">
            <v-btn class="text-white" variant="text" @click="dialog = false">
              <p class="text-white">
                Fechar
              </p>
            </v-btn>
          </v-toolbar-items>
        </v-toolbar>

        <!--  -->

        <div class="DetalhesProdutoInvestir">

          <div class="DetalhesProdutoInvestirFilho1">
            <div class="fundoSlogamHistory">
              <p class="text-white slogamFazenda d-flex flex-column justify-space-between" style="height: 400px;">
                <div></div>
                <span class="marcaSlogam">CENOURA NACIONAL</span>
              </p>
            </div>
          </div>

          <div class="DetalhesProdutoInvestirFilho2">
            <div>
              <table>

                <tr class="CapitalPInvestir">
                  <td>Fazenda</td>
                  <th>MUMBA</th>
                </tr>


                <tr class="CapitalPInvestir">
                  <td>Início do processo de plantio da cultura</td>
                  <th>13-03-2022</th>
                </tr>

                <tr class="CapitalPInvestir">
                  <td>Fim do processo de produção</td>
                  <th>20-07-2022</th>
                </tr>

                <tr class="CapitalPInvestir">
                  <td>Produto</td>
                  <th>Cenoura Nacional</th>
                </tr>

                <tr class="CapitalPInvestir">
                  <td>Área de Produção</td>
                  <th>2.000 HECTARES</th>
                </tr>

                <tr class="CapitalPInvestir">
                  <td>Fases da Produção</td>
                  <th>Todas</th>
                </tr>

                <tr class="CapitalPInvestir">
                  <td>Tempo de Produção</td>
                  <th>4 Meses</th>
                </tr>

                <tr class="CapitalPInvestir">
                  <td>Quantidade estimada</td>
                  <th>20.000 Toneladas</th>
                </tr>

                <tr class="CapitalPInvestir">
                  <td>Quantidade colhida</td>
                  <th>18.000 Toneladas</th>
                </tr>

                <tr class="CapitalPInvestir">
                  <td>Capital Solicitado</td>
                  <th>3.722.000</th>
                </tr>

                <tr class="CapitalPInvestir">
                  <td>Taxa de Retorno</td>
                  <th>16%</th>
                </tr>

                <tr class="CapitalPInvestir">
                  <td>Valor Total da Venda</td>
                  <th>13.000,20 Kz</th>
                </tr>

              </table>
 
            </div>
          </div>


        </div>

        <div class="inicioInvestidor SolicitacaoFinanceamento">
          <div class="sia-cardSolicitacao">
            <table>
              <tr>
                <td rowspan="2">
                  <div class="icon-fazenda"></div>
                </td>
                <td style="vertical-align: bottom;">
                  <h2 class="title h2Solicitacao" style="margin-left: 15px;">Faça Simulações de Investimento</h2>
                </td>
              </tr>
              <tr>
                <td style="vertical-align: top;">
                  <p class="desc pInvista" style="margin-left: 15px;">Aplique o montante desejado e Simule um Investimento...</p>
                </td>
              </tr>
            </table>
          </div>
        </div>

        <div class="PocicaoTabelasDetalhesProdutosFinanciar">
          <v-card>
            <template v-slot:prepend>

              <div class="text-center d-flex pb-4">
                <v-btn class="ma-2" @click="all">
                  Simular Investimento
                </v-btn>
              </div>

              <!-- <div class="pb-4">v-model {{ panel }}</div> -->

              <div class="DetalhesProcessoInvestimento">
                <v-expansion-panels v-model="panel" multiple>
                  <v-expansion-panel title="Testar Agora">
                    <v-expansion-panel-text>
                      <div class="InfoPainel">
                        Erivaldo Albano
                      </div>
                    </v-expansion-panel-text>

                  </v-expansion-panel>

                </v-expansion-panels>
              </div>

            </template>
          </v-card>
        </div>



        <!--  -->

      </v-card>
    </v-dialog>
  </v-row>
</template>
<script>
export default {
  data() {
    return {
      dialog: false,
      notifications: false,
      sound: true,
      widgets: false,


      desserts: [
        {
          name: '10.000.000 Kz',
          cRisco: '2.300.000 Kz',
          cGiro: '7.700.000 Kz',
          cRetorno: '60.000.000 Kz',
          tProducao: '4',
          iProducao: '20/07/2023'
        },

        {
          name: '10.000.000 Kz',
          cRisco: '2.300.000 Kz',
          cGiro: '7.700.000 Kz',
          cRetorno: '60.000.000 Kz',
          tProducao: '4',
          iProducao: '20/01/2023'
        },

      ],


      // Analid=se de Risco de Investimento

      dessertsRiscosIvestimentos: [
        {
          descricaoRisco: 'Análise de solo e preparação',
          valorRisco: '500.000Kz',
          percentagem: '5.00%',
        },

        {
          descricaoRisco: 'Furo de água',
          valorRisco: '500.000Kz',
          percentagem: '5.00%',
        },
        {
          descricaoRisco: 'Materiais',
          valorRisco: '300.000Kz',
          percentagem: '3.00%',
        },
        {
          descricaoRisco: 'Obrigações Juridicas',
          valorRisco: '500.000Kz',
          percentagem: '5.00%',
        },
        {
          descricaoRisco: 'Obrigações Tributarias',
          valorRisco: '300.000Kz',
          percentagem: '3.00%',
        },
        {
          descricaoRisco: 'Conta Corrente',
          valorRisco: '700.000Kz',
          percentagem: '7.00%',
        },
        {
          descricaoRisco: 'Total',
          valorRisco: '2.300.000Kz',
          percentagem: '23.00%',
        },
      ],

      // Fim da Analise de Risco de Investimento


      // 
      dessertsCapitalGiroIvestimentos: [
        {
          descricaoGiro: 'Sementes',
          qtdGiro: '641.67un.',
          precoAquisicaoGiro: '12.000Kz',
          totalGiro: '7.700.000Kz',
          percentagemGiro: '77.00%',
        }

      ],
      //


      // 
      dessertsCapitalRetornoIvestimentos: [
        {
          descricaoRetorno: 'Kilo',
          qtdRetorno: '641.67un.',
          precoMercadoRetorno: '10.000Kz',
          totalRetorno: '60.000.000Kz',
          percentagemRetorno: '600%',
        }

      ],
      //


      panel: [],
      methods: {
        all() {
          this.panel = ['foo', 'bar', 'baz']
        },
        none() {
          this.panel = []
        },
      },

      colors: [
        '#fff',
        '#fff',
        '#fff',
      ],
      slides: [
        'First',
        'Second',
        'Third',
      ],
    }
  },
}
</script>
<style>
.dialog-bottom-transition-enter-active,
.dialog-bottom-transition-leave-active {
  transition: transform .2s ease-in-out;
}
</style>