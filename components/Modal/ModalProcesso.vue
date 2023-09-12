<style>
.DetalhesProcessoInvestimento {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 0 auto;
  width: 1200px;
}

.InfoPainel {
  box-shadow: rgba(99, 99, 99, 0.2) 0px 2px 8px 0px;
}



.DetalhesProduto {
  width: 1250px;
  display: grid;
  justify-content: center;
  align-items: center;
  margin: 0 auto;
  margin-bottom: 20px;
  grid-template-columns: repeat(2, 1fr);
  box-shadow: rgba(50, 50, 93, 0.25) 0px 50px 100px -20px, rgba(0, 0, 0, 0.3) 0px 30px 60px -30px;
  box-shadow: rgba(0, 0, 0, 0.16) 0px 10px 36px 0px, rgba(0, 0, 0, 0.06) 0px 0px 0px 1px;
  box-shadow: rgba(50, 50, 93, 0.25) 0px 50px 100px -20px, rgba(0, 0, 0, 0.3) 0px 30px 60px -30px;
  padding: 10px;
}

.DetalhesProdutoFilho1 {
  width: 100%;
}

.DetalhesProdutoFilho2 {
  width: max-content;
}

.SlideProdutos img {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 0 auto;
  width: 80%;
  height: 100%;

}

.PocicaoTabelasDetalhes {
  display: grid;
  justify-content: center;
  align-items: center;
  margin: auto;
  margin-top: 20px;
  width: 1099px;
}

.InfoPainel {
  display: grid;
  justify-content: center;
  align-items: center;
  box-shadow: rgba(0, 0, 0, 0.15) 0px 5px 15px 0px;
}

.TabelaRiscos {
  width: 1200px;
}



/* Responsive table styles */
.responsiveTable {
  border-collapse: collapse;
  margin: 0;
  padding: 0;
  width: 100%;
  table-layout: fixed;
}

.responsiveTable caption {
  font-size: 1rem;
  /* margin: 0.5rem 0 0.75rem; */
}

.responsiveTable tr {
  border-bottom: 1px solid #d1d1d161;
  /* padding: 0.5rem; */
}

.responsiveTable th,
.responsiveTable td {
  /* padding: 0.625rem; */
  text-align: left;
}

.responsiveTable th {
  font-size: 1rem;
  font-weight: 700;
  border-bottom: 2px solid #8f8f8f6e;
}

@media screen and (max-width: 999px) {

  .responsiveTable {
    border: 0;
  }


  .responsiveTable caption {
    font-size: 1rem;
  }

  .responsiveTable thead {
    clip: rect(0 0 0 0);
    height: 1px;
    margin: -1px;
    overflow: hidden;
    padding: 0;
    position: absolute;
    width: 1px;
  }

  .responsiveTable tr {
    border-bottom: 3px solid #ddd;
    display: block;
    margin-bottom: 0.625rem;
    padding: 0;
  }

  .responsiveTable td {
    border-bottom: 1px solid #ddd;
    display: block;
    font-size: 1rem;
    text-align: right;
  }

  .responsiveTable td::before {
    /*************************************************************************
      ** aria-label has no advantage, it won't be read inside a .responsiveTable
      content: attr(aria-label);================================================
      **************************************************************************/
    content: attr(data-label);
    float: left;
    font-weight: 700;
    text-transform: uppercase;
    font-size: 0.9rem;
  }

  .responsiveTable td:last-child {
    border-bottom: 0;
  }
}



/** Responsividade da parte de investimento  */

@media(max-width:900px) {
  .DetalhesProduto {
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


}

.azulBI {
  display: none;
  background: #0b5ed7;
  width: 100%;
  height: 60px;
  margin-bottom: 10px;
}

@media(max-width:999px) {
  .azulBI {
    display: block;
  }
}
</style>

<template>
  <v-row justify="center">
    <v-dialog class="" v-model="dialog" fullscreen :scrim="false" transition="dialog-bottom-transition">
      <template v-slot:activator="{ props }">
        <v-btn dark v-bind="props">
          <p class="btnProcessoInvestir">Abrir</p>
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
              Processo de Investimento
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
        <v-list lines="two" subheader>
          <v-list-subheader>Detalhes do (s) Produto (s) em Investimento</v-list-subheader>

        </v-list>

        <!--  -->


        <div class="DetalhesFazenda">

          <div class="DetalhesFazendaFilho1">
            <div class="fundoSlogam">
              <p class="text-white slogamFazenda">
                DA NOSSA TERRA <span class="marcaSlogam"> PARA A SUA MESA</span>
              </p>
            </div>
          </div>

          <div class="DetalhesFazendaFilho2">
            <div>
              <table>
                <tr>
                  <td>Fazenda</td>
                  <th>MUMBA</th>
                </tr>

                <tr>
                  <td>Localização</td>
                  <th>Provincia da Huila</th>
                </tr>

                <tr>
                  <td>Área Total</td>
                  <th>90.000 HECTARES</th>
                </tr>

                <tr>
                  <td>Sede</td>
                  <th>Bairro de Tchioco</th>
                </tr>

                <tr>
                  <td>Telefone</td>
                  <th>+244 934 337 822</th>
                </tr>

                <tr>
                  <td>Email</td>
                  <th>info.ao@omatapalo.com</th>
                </tr>
                <tr>
                  <td>Site</td>
                  <th>www.omatapalo.com</th>
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
                  <h2 class="title h2Solicitacao" style="margin-left: 15px;">Produtos com Financeamento</h2>
                </td>
              </tr>
              <tr>
                <td style="vertical-align: top;">
                  <p class="desc pInvista" style="margin-left: 15px;">Financeamento na Produção MUMBA...</p>
                </td>
              </tr>
            </table>
          </div>
        </div>


        <div class="ProdutosDaFazenda">
          <v-container class="CardsFazenda">
            <v-row>
              <v-col cols="12" sm="3" md="3">

                <v-card class="mx-auto" max-width="300">
                  <v-img class="align-end text-white imageProduto" height="180" src="" cover></v-img>

                  <v-card-subtitle class="pt-4">
                    Batata Rena Nacional
                  </v-card-subtitle>

                  <v-card-actions>
                    <ModalDetalhesFinancementoProduto />
                  </v-card-actions>
                </v-card>

              </v-col>

              <v-col cols="12" sm="3" md="3">

                <v-card class="mx-auto" max-width="300">
                  <v-img class="align-end text-white imageProduto3" height="180" src="" cover></v-img>

                  <v-card-subtitle class="pt-4">
                    Couve Nacional
                  </v-card-subtitle>

                  <v-card-actions>
                    <v-btn color="" class="btnVerFazenda text-white">
                      <ModalDetalhesFinancementoProduto />
                    </v-btn>
                  </v-card-actions>
                </v-card>

              </v-col>

              <v-col cols="12" sm="3" md="3">

                <v-card class="mx-auto" max-width="300">
                  <v-img class="align-end text-white imageProduto2" height="180" src="" cover></v-img>

                  <v-card-subtitle class="pt-4">
                    Tomate Nacional
                  </v-card-subtitle>

                  <v-card-actions>
                    <v-btn color="" class="btnVerFazenda text-white">
                      <ModalDetalhesFinancementoProduto />
                    </v-btn>

                  </v-card-actions>
                </v-card>

              </v-col>


              <v-col cols="12" sm="3" md="3">

                <v-card class="mx-auto" max-width="300">
                  <v-img class="align-end text-white imageProduto1" height="180" src="" cover></v-img>

                  <v-card-subtitle class="pt-4">
                    Cebola Nacional
                  </v-card-subtitle>

                  <v-card-actions class="text-white">
                    <v-btn color="" class="btnVerFazenda text-white">
                      <ModalDetalhesFinancementoProduto />
                    </v-btn>

                  </v-card-actions>
                </v-card>

              </v-col>
            </v-row>
          </v-container>
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