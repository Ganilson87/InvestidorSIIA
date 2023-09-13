<style>
.inicioInvestidor {
    padding: 20px;
}

.inicioInvestidor h2 {
    color: #0b5ed7;
}

.CardsInicioDashboard {
    padding: 10px;
}

.PrimeiraTabelaFazendas {
    margin: 13px;
    width: 300px;
}

.espacoTabela {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    margin: 15px;
    gap: 15px;  
    padding: 10px; 
}

.tabelaFazendaAplicacao{
    width: 750px;
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
}

.espacoSegundaTabela{
    display: grid;
    margin: 25px;
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
}

.graficoFazendaAplicacao {
    background: #fff;
    width: 100%; 
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
}

.graficoFazendaAplicacao p { 
    color: #000;
    font-size: 1.2rem;
    text-align: center;
    margin: 10px;
}

.GraficoTaxaRetorno{
    width: 100%;
    height: 100%;  
}

.Fundothead {
    background: #0b5ed7;
    color: #fff;
}

.Fundothead th {
    color: #fff;
}

.sia-card-1 {
    position: relative;
    background-color: #aaaaaa63;
    border-radius: 10px;
    padding: 20px;
}

.sia-card-1 td {
    padding: 0 !important;
}

.sia-card-1 .icon-notf {
    width: 60px;
    height: 60px;
    background-color: #aaaaaa63;
    border-radius: 10px;
}

.sia-card-1 .title,
.sia-card-1 .desc {
    padding: 0 20px;
}

.icon-notf1 {
    background: url(../public/img/provincias/Benguela.jpeg);
    background-position: center;
    background-size: cover;
    border-radius: 10px;
    width: 60px;
    height: 60px;
}

.icon-notf2 {
    background: url(../public/img/provincias/huila.jpeg);
    background-position: center;
    background-size: cover;
    border-radius: 10px;
    width: 60px;
    height: 60px;
}

/* Formatacao de estilo da modal para a abertura do processo do investimento */

.dialog-bottom-transition-enter-active,
.dialog-bottom-transition-leave-active {
    transition: transform .2s ease-in-out;
}

/* Fim da Modal */

/*  */
.CardsInicioDahs {
    width: 96%;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    justify-content: center;
    align-items: center;
    margin: 0 auto;
    gap: 25px;
}

.CardsInicioDahs h3 {
    font-size: 1.3rem;
    font-weight: 100;
    padding: 10px;
}

.CardsInicioDahs span {
    font-size: 2rem;
    padding: 10px;
}

.cardInicio1,
.cardInicio2,
.cardInicio3 {
    width: 100%;
    height: 140px;
    background: #fff;
    box-shadow: rgba(0, 0, 0, 0.15) 0px 5px 15px 0px;
    border-radius: 4px;
}

.infoCairdDahs {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
}


.iconDash img {
    width: 40px;
    height: 40px;
    border-radius: 50%;
}

/*  */

/* Responsividade */

@media(max-width:870px) {
    .CardsInicioDahs {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
    }
}

@media(max-width:500px) {
    .CardsInicioDahs {
        display: grid;
        grid-template-columns: repeat(1, 1fr);
    }
}

@media(max-width:999px) {
    .espacoTabela {
        display: grid;
        grid-template-columns: repeat(1, 1fr);
    }

}

/*  */


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
    <div class="inicioInvestidor">
        <h2>SIIIA | FINANCIADOR</h2>
        <p> Sistema Integrado de Investimento e Inclusão Agrária</p>
    </div>

    <div class="CardsInicioDahs">
        <div class="cardInicio1">
            <h3>Solicitações de Financiamento</h3>
            <div class="infoCairdDahs">
                <div>
                    <span>2</span>
                </div>

                <div class="iconDash">
                    <img src="../public/img/fazendas/faz.jpeg" alt="">
                </div>
            </div>
        </div>

        <div class="cardInicio2">
            <h3>Meus Investimentos</h3>
            <div class="infoCairdDahs">
                <div>
                    <span>8</span>
                </div>

                <div class="iconDash">
                    <img src="../public/img/fazendas/fazenda.jpeg" alt="">
                </div>
            </div>
        </div>
        <div class="cardInicio3">
            <h3>Investimentos com Retorno</h3>
            <div class="infoCairdDahs">
                <div>
                    <span>2</span>
                </div>

                <div class="iconDash">
                    <img src="../public/img/fazendas/fazenda1.jpeg" alt="">
                </div>
            </div>
        </div>
    </div>

    <br>

    <div class="CardsInicioDahs">
        <div class="cardInicio1">
            <h3>Produtos em Alta no Mercado</h3>
            <div class="infoCairdDahs">
                <div>
                    <span></span>
                </div>
 
            </div>
        </div>


    </div>

    <!-- tabela de fazendas com o meu investimento -->

    <div class="inicioInvestidor">
        <div class="sia-card-1">
            <table>
                <tr>
                    <td rowspan="2">
                        <div class="icon-notf1"></div>
                    </td>
                    <td style="vertical-align: bottom;">
                        <h2 class="title h2Solicitacao">Portfólio de investimentos</h2>
                    </td>
                </tr>
                <tr>
                    <td style="vertical-align: top;">
                        <p class="desc pInvista">Detalhes de todos os seus investimentos...</p>
                    </td>
                </tr>
            </table>
        </div>
    </div>

    <div class="azulBI"></div>

    <div class="espacoTabela">

        <div class="tabelaFazendaAplicacao">
            <v-table height="300px" class="PrimeiraTabelaFazendas responsiveTable">

                <thead class="Fundothead">
                    <tr>
                        <th class="text-white">
                            Fazenda
                        </th>

                        <th class="text-white">
                            Capital Investido
                        </th>
                        <th class="text-white">
                            Duração
                        </th>

                        <th class="text-white">
                            Processo
                        </th>
                    </tr>
                </thead>

                <tbody>
                    <tr v-for="item in desserts" :key="item.name">
                        <td data-label="fazenda">{{ item.name }}</td>
                        <td data-label="capital">{{ item.capital }}</td>
                        <td data-label="duração">{{ item.duracao }}</td>
                        <td data-label="detalhes">
                            <ModalProcesso />
                        </td>
                    </tr>
                </tbody>
            </v-table>
        </div>

        <div class="graficoFazendaAplicacao">
            <div class="GraficoTaxaRetorno">
                <P class="">
                Taxa de retorno do investimento
            </P>
                <ModalGraficoInvestimento />
            </div>
        </div>

    </div>

    <!--  -->

    <div class="inicioInvestidor">
        <div class="sia-card-1">
            <table>
                <tr>
                    <td rowspan="2">
                        <div class="icon-notf2"></div>
                    </td>
                    <td style="vertical-align: bottom;">
                        <h2 class="title h2Solicitacao">Sugestões de Investimento para sí</h2>
                    </td>
                </tr>
                <tr>
                    <td style="vertical-align: top;">
                        <p class="desc pInvista">Investimentos que a sua carteira pode cobrir e render retornos...</p>
                    </td>
                </tr>
            </table>
        </div>
    </div>

    <div class="azulBI"></div>
    <div class="espacoSegundaTabela">
        <v-table height="300px" class="PrimeiraTabelaFazendas responsiveTable">

            <thead class="Fundothead">
                <tr>
                    <th class="text-white">
                        Fazenda
                    </th>
                    <th class="text-white">
                        Produto
                    </th>
              
                    <th class="text-white">
                        Valor solicitado
                    </th>
                    <th class="text-white">
                        Duração
                    </th>
                    <th class="text-white">
                        Taxa de Retorno (%)
                    </th>

                    <th class="text-white">
                        Investir
                    </th>
                </tr>
            </thead>

            <tbody>
                <tr v-for="item in dessertsFazenda" :key="item.nameFazenda">
                    <td data-label="Fazenda">{{ item.nameFazenda }}</td>
                    <td data-label="produto">{{ item.produtoFazenda }}</td> 
                    <td data-label="caoital">{{ item.capitalFazenda }}</td>
                    <td data-label="duração">{{ item.duracaoFazenda }}</td>
                    <td data-label="taxa %">{{ item.taxaFazenda }}</td>
                    <td data-label="">
                        <ModalFinancear />
                    </td>
                </tr>
            </tbody>
        </v-table>
    </div>
</template>

<!-- Funcoes -->  

<script>
export default {
    data() {
        return {

            // Funcao para abrir a modal de informacao do processo do investimento  


            // Tabela de segestao de investimentos

            dessertsFazenda: [
                {
                    nameFazenda: 'AgroSol',
                    capitalFazenda: '33.143.00',
                    duracaoFazenda: '4 Meses',
                    produtoFazenda: 'Batata Rena Nacional',
                    taxaFazenda: '14%',
                },

                {
                    nameFazenda: 'Mumba',
                    capitalFazenda: '13.113.00',
                    duracaoFazenda: '3 Meses',
                    produtoFazenda: 'Tomate Nacional',
                    taxaFazenda: '14%',
                },
            ],

            // Funcao para lista de investimentos feitos nas fazendas

            desserts: [
                {
                    name: 'Mumba',
                    capital: '1.400.00',
                    duracao: '6 Meses',
                    processo: 'Abrir'
                },
                {
                    name: 'NNN',
                    capital: '3.900.00',
                    duracao: '2 Meses',
                    processo: 'Abrir'
                },
                {
                    name: 'Lubamba',
                    capital: '4.100.00',
                    duracao: '3 Meses',
                    processo: 'Abrir'
                },
                {
                    name: 'Luas',
                    capital: '3.000.00',
                    duracao: '12 Meses',
                    processo: 'Abrir'
                },
                {
                    name: 'Zacarias',
                    capital: '13.900.00',
                    duracao: '8 Meses',
                    processo: 'Abrir'
                },
                {
                    name: 'Lubamba',
                    capital: '900.00',
                    duracao: '6 Meses',
                    processo: 'Abrir'
                },
                {
                    name: 'Freitas',
                    capital: '9.000.00',
                    duracao: '9 Meses',
                    processo: 'Abrir'
                },
                {
                    name: 'AgroSol',
                    capital: '3.900.00',
                    duracao: '6 Meses',
                    processo: 'Abrir'
                },



            ],
        }

    },
}
</script>

<!-- Funcao Para abertura da modal -->

<!-- Fim da Funcao de abertura da -->

