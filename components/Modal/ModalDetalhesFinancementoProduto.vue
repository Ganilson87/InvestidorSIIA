<style>
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

.fundoSlogam {
  padding: 20px;
  width: 100%;
  backdrop-filter: blur(4px);
  background: #ffffff41;
  margin-top: 210px;
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

.bb{
  position: absolute;
  width: 100%;
  height: 100%;
  top: 65px; 
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
              Detalhes do Produto Investido
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

        <div class="bb"> 
          <ModalAnimacaoMonye />
        </div>
        
        <div class="DetalhesProdutoInvestir">

          <div class="DetalhesProdutoInvestirFilho1">
            <div class="fundoSlogam">
              <p class="text-white slogamFazenda">
                <span class="marcaSlogam">BATATA RENA NACIONAL</span>
              </p>
            </div>
          </div>

          <div class="DetalhesProdutoInvestirFilho2">
            <div>
              <table>
                <tr>
                  <td>Fazenda</td>
                  <th>MUMBA</th>
                </tr>

                <tr>
                  <td>Produto</td>
                  <th>Batata Rena Nacional</th>
                </tr>

                <tr>
                  <td>Área de Produção</td>
                  <th>2.000 HECTARES</th>
                </tr>

                <tr class="CapitalPInvestir">
                  <td>Fase da Produção</td>
                  <th>Plantio</th>
                </tr>

                <tr>
                  <td>Tempo de Produção</td>
                  <th>7 Meses</th>
                </tr>

                <tr>
                  <td>Quantidade estimada</td>
                  <th>30.000 Toneladas</th>
                </tr>

                <tr>
                  <td>Capital Solicitado</td>
                  <th>33.782,20 Kz</th>
                </tr>

                <tr>
                  <td>Taxa de Retorno</td>
                  <th>16%</th>
                </tr>

                <tr class="CapitalPInvestir">
                  <td>Capital Investido</td>
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
                  <h2 class="title h2Solicitacao" style="margin-left: 15px;">Acompanhamento da evolução do processo produtivo</h2>
                </td>
              </tr>
              <tr>
                <td style="vertical-align: top;">
                  <p class="desc pInvista" style="margin-left: 15px;">Confira tudo, desde as fazes de produção até análises de risco, capital de giro e retorno...</p>
                </td>
              </tr>
            </table>
          </div>
        </div>

        <div class="ProcessoProducao">

          <v-timeline side="end">
            <v-timeline-item dot-color="green-lighten-2" fill-dot>
              <v-card>
                <v-card-title class="bg-green-lighten-2"> 
                  <h2 class="font-weight-light text-white">
                    Plantio
                  </h2>
                </v-card-title>
                <v-card-text>
             <p class="espacoText">
              Cuidados com a Plantação: Durante o período de crescimento, as plantas requerem cuidados contínuos, como irrigação, controle de pragas e doenças, e a aplicação de mais fertilizantes, se necessário.
             </p> 
             <p class="espacoText">
              Monitoramento: Os agricultores monitoram o crescimento das culturas, verificando se há problemas e ajustando as práticas de cultivo conforme necessário.
             </p>
                </v-card-text>
              </v-card>
            </v-timeline-item>
            

            <v-timeline-item dot-color="amber-lighten-1" fill-dot>
              <v-card>
                <v-card-title class="bg-amber-lighten-1 justify-end"> 
                  <h2 class="me-4 font-weight-light text-white">
                    Colheita
                  </h2>
                </v-card-title>
                <v-card-text>
                 <p class="espacoText">
                  Determinação da Maturidade: A colheita da cultura atingio a maturidade. Isso é importante para garantir a qualidade do produto.  
                 </p> 
                 <p class="espacoText">
                  Processamento: Algumas culturas requerem processamento imediato após a colheita, como lavagem, descascamento ou embalagem. Isso preserva a qualidade e aumenta a vida útil.
                 </p>
                </v-card-text>
              </v-card>
            </v-timeline-item>

            <v-timeline-item dot-color="cyan-lighten-1" fill-dot>
              <v-card>
                <v-card-title class="bg-cyan-lighten-1">
                  <!-- <v-icon class="me-4" size="large" icon="mdi-email-outline"></v-icon> -->
                  <h2 class="font-weight-light text-white">
                    Armazenamento
                  </h2>
                </v-card-title>
                <v-card-text>
                  <p class="espacoText">
                    Os produtos colhidos são armazenados em locais apropriados. O armazenamento é crucial para evitar perdas devido a condições climáticas adversas ou pragas.
                  </p>
                </v-card-text>
              </v-card>
            </v-timeline-item>

            <v-timeline-item dot-color="red-lighten-1" fill-dot size="x-small">
              <v-card>
                <v-card-title class="bg-red-lighten-1 justify-end">
                  <h2 class="me-4 font-weight-light text-white">
                    Venda
                  </h2>
                  <!-- <v-icon size="large" icon="mdi-account-multiple-outline"></v-icon> -->
                </v-card-title>
                <v-card-text>
                  <p class="espacoText">
                    Mercado e Distribuição: Os agricultores podem vender seus produtos diretamente em mercados locais, por meio de intermediários ou para grandes distribuidores. A escolha depende da escala da operação e das preferências do agricultor.
                  </p>
                </v-card-text>
              </v-card>
            </v-timeline-item>
            
          </v-timeline>

        </div>

        <div class="PocicaoTabelasDetalhesProdutosFinanciar">
          <v-card>
            <template v-slot:prepend>

              <div class="text-center d-flex pb-4">
                <v-btn class="ma-2" @click="all">
                  Abrir Todos
                </v-btn>
                <v-btn class="ma-2" @click="none">
                  Fechar
                </v-btn>
              </div>

              <!-- <div class="pb-4">v-model {{ panel }}</div> -->

              <div class="DetalhesProcessoInvestimento">
                <v-expansion-panels v-model="panel" multiple>
                  <v-expansion-panel title="Análise de Risco">
                    <v-expansion-panel-text>
                      <div class="InfoPainel">
                        <v-table height="300px" class="TabelaRiscos">
                          <thead class="Fundothead">
                            <tr>
                              <th class="text-white">
                                Descrição
                              </th>
                              <th class="text-white">
                                Valor
                              </th>
                              <th class="text-white">
                                Percentágem
                              </th>
                            </tr>
                          </thead>

                          <tbody>
                            <tr v-for="item in dessertsRiscosIvestimentos" :key="item.descricaoRisco">
                              <td>{{ item.descricaoRisco }}</td>
                              <td>{{ item.valorRisco }}</td>
                              <td>{{ item.percentagem }}</td>
                            </tr>
                          </tbody>
                        </v-table>
                      </div>
                    </v-expansion-panel-text>

                  </v-expansion-panel>

                  <v-expansion-panel title="Capital de Giro">
                    <v-expansion-panel-text
                    style="max-height: 120px;"
                    >
                      <div class="InfoPainel">
                        <v-table height="300px" class="TabelaRiscos">
                          <thead class="Fundothead">
                            <tr>
                              <th class="text-white">
                                Descrição
                              </th>
                              <th class="text-white">
                                Quantidade
                              </th>
                              <th class="text-white">
                                Preço de Aquisição
                              </th>
                              <th class="text-white">
                                Total
                              </th>
                              <th class="text-white">
                                Porcentagem
                              </th>
                            </tr>
                          </thead>

                          <tbody>
                            <tr v-for="item in dessertsCapitalGiroIvestimentos" :key="item.descricaoGiro">
                              <td>{{ item.descricaoGiro }}</td>
                              <td>{{ item.qtdGiro }}</td>
                              <td>{{ item.precoAquisicaoGiro }}</td>
                              <td>{{ item.totalGiro }}</td>
                              <td>{{ item.percentagemGiro }}</td>
                            </tr>
                          </tbody>
                        </v-table>
                      </div>
                    </v-expansion-panel-text>

                  </v-expansion-panel>

                  <v-expansion-panel title="Capital de Retorno">
                    <v-expansion-panel-text 
                    style="max-height: 120px;"
                    >
                      <div class="InfoPainel">
                        <v-table height="300px" class="TabelaRiscos">
                          <thead class="Fundothead">
                            <tr>
                              <th class="text-white">
                                Descrição
                              </th>
                              <th class="text-white">
                                Quantidade
                              </th>

                              <th class="text-white">
                                Preço de Mercado
                              </th>
                              <th class="text-white">
                                Total
                              </th>
                              <th class="text-white">
                                Percentagem
                              </th>
                            </tr>
                          </thead>

                          <tbody>
                            <tr v-for="item in dessertsCapitalRetornoIvestimentos" :key="item.descricaoRetorno">
                              <td>{{ item.descricaoRetorno }}</td>
                              <td>{{ item.qtdRetorno }}</td>
                              <td>{{ item.precoMercadoRetorno }}</td>
                              <td>{{ item.totalRetorno }}</td>
                              <td>{{ item.percentagemRetorno }}</td>
                            </tr>
                          </tbody>
                        </v-table>
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