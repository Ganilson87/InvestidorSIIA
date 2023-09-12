<style>
.CardsFazenda {
    justify-content: center;
    align-items: center;
    margin: 0 auto;
}

.btnVerFazenda {
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 0 auto;
    width: 100%;
    background: #0b5ed7;
    color: #fff;
    transition: 1s;
}

.btnVerFazenda:hover {
    background: #1f76f9da;
    transition: 1s;
}

.imageFazenda1 {
    background: url(../../public/img/fazendas/faz.jpeg);
    background-position: center;
    background-size: cover;
    width: 100%;
    height: 100%;
}

.imageFazenda2 {
    background: url(../../public/img/fazendas/fase.jpeg);
    background-position: center;
    background-size: cover;
    width: 100%;
    height: 100%;
}

.imageFazenda3 {
    background: url(../../public/img/fazendas/fazenda.jpeg);
    background-position: center;
    background-size: cover;
    width: 100%;
    height: 100%;
}

.imageFazenda4 {
    background: url(../../public/img/fazendas/fazenda1.jpeg);
    background-position: center;
    background-size: cover;
    width: 100%;
    height: 100%;
}

.FundoFazenda {
    width: 100%;
    height: 100%;
    background: #0b5dd742;
}

/**Nova Formatacao do layout das Fazendas */

.paiFazendas {
    display: grid;
    justify-content: center;
    align-items: center;
    margin: auto;
    grid-template-columns: repeat(4, 1fr); 
    width: 100%;
    padding: 5px; 
    gap: 10px;
}

.filhoFazenda{
    display: grid; 
    width: 100%;
    background: #fff;
    padding: 10px;
    border-radius: 7px;
}

p.txtFazenda{
    width: 100%; 
    padding: 10px;
    font-size: 1.2rem;
    font-weight: bold;
    background: #0b5dd74b;
    margin-top: 130px;
}
.txtFazendaP{
    margin: 10px;
    font-size: 0.9rem;
}
.imgFazenda1{
    background: url(../../public/img/fazendas/faz.jpeg);
    background-position: center;
    background-size: cover;
    width: 100%;
    max-height: 180px;
}
.imgFazenda2{
    background: url(../../public/img/fazendas/fazenda1.jpeg);
    background-position: center;
    background-size: cover;
    width: 100%;
    max-height: 180px;
}
.imgFazenda3{
    background: url(../../public/img/fazendas/fase.jpeg);
    background-position: center;
    background-size: cover;
    width: 100%;
    max-height: 180px;
}
.imgFazenda4{
    background: url(../../public/img/fazendas/fazenda.jpeg);
    background-position: center;
    background-size: cover;
    width: 100%;
    max-height: 180px;
}


/** Responsividade da Lista de Fazendas */

@media(max-width: 1284px){
    .paiFazendas {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
}

}

@media(max-width:999px){
    .paiFazendas {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
}

}

@media(max-width:529px){
    .paiFazendas {
    display: grid;
    grid-template-columns: repeat(1, 1fr);
}

}
</style>

<template>
    <div class="inicioInvestidor">
        <h2>SIIIA | FAZENDAS</h2>
        <p> Sistema Integrado de Investimento e Inclusão Agrária</p>
    </div>

    <!-- <v-container class="CardsFazenda">
        <v-row>
            <v-col cols="12" sm="3" md="3">

                <v-card class="mx-auto" max-width="300">
                    <v-img class="align-end text-white imageFazenda1" height="180" src="" cover>
                        <div class="FundoFazenda">
                            <v-card-title class="text-white">FAZENDA MUMBA</v-card-title>
                        </div>
                    </v-img>

                    <v-card-subtitle class="pt-4">
                        PROVINCIA DA HUILA
                    </v-card-subtitle>

                    <v-card-actions>
                        <ModalProdutoFazenda />
                    </v-card-actions>
                </v-card>

            </v-col>

            <v-col cols="12" sm="3" md="3">

                <v-card class="mx-auto" max-width="300">
                    <v-img class="align-end text-white imageFazenda4" height="180" src="" cover>
                        <div class="FundoFazenda">
                            <v-card-title class="text-white">FAZENDA TCHISSOLA</v-card-title>
                        </div>
                    </v-img>

                    <v-card-subtitle class="pt-4">
                        PROVINCIA DA HUILA
                    </v-card-subtitle>

                    <v-card-actions>
                        <v-btn color="" class="btnVerFazenda text-white">
                            <P class="text-white">ABRIR</P>
                        </v-btn>
                    </v-card-actions>
                </v-card>

            </v-col>

            <v-col cols="12" sm="3" md="3">

                <v-card class="mx-auto" max-width="300">
                    <v-img class="align-end text-white imageFazenda3" height="180" src="" cover>
                        <div class="FundoFazenda">
                            <v-card-title class="text-white">FAZENDA GIRASSOL</v-card-title>
                        </div>
                    </v-img>

                    <v-card-subtitle class="pt-4">
                        PROVINCIA DA HUILA
                    </v-card-subtitle>

                    <v-card-actions>
                        <v-btn color="" class="btnVerFazenda text-white">
                            <P class="text-white">ABRIR</P>
                        </v-btn>

                    </v-card-actions>
                </v-card>

            </v-col>

            <v-col cols="12" sm="3" md="3">

                <v-card class="mx-auto" max-width="300">
                    <v-img class="align-end text-white imageFazenda2" height="180" src="" cover>
                        <div class="FundoFazenda">
                            <v-card-title class="text-white">FAZENDA JAMBA</v-card-title>
                        </div>
                    </v-img>

                    <v-card-subtitle class="pt-4">
                        PROVINCIA DA HUILA
                    </v-card-subtitle>

                    <v-card-actions class="text-white">
                        <v-btn color="" class="btnVerFazenda text-white">
                            <P class="text-white">ABRIR</P>
                        </v-btn>

                    </v-card-actions>
                </v-card>

            </v-col>
        </v-row>
    </v-container> -->


    <!-- <h2 class="text-center">Nova Formatacao Do Layout da FAZENDA</h2> -->

    <div class="paiFazendas">
        <div class="filhoFazenda">
            <div class="imgFazenda1">
                <p class="txtFazenda text-white">FAZENDA JAMBA</p>
            </div>
            <div>
                <p class="txtFazendaP">PROVINCIA DA HUILA</p>
            </div>
            <div>
                <v-card-actions>
                    <ModalProdutoFazenda />
                </v-card-actions>
            </div>
        </div>

        <div class="filhoFazenda">
            <div class="imgFazenda2">
                <p class="txtFazenda text-white">FAZENDA GIRASSOL</p>
            </div>
            <div>
                <p class="txtFazendaP">PROVINCIA DA HUILA</p>
            </div>
            <div>
                <v-card-actions>
                    <ModalProdutoFazenda />
                </v-card-actions>
            </div>
        </div>

        <div class="filhoFazenda">
            <div class="imgFazenda3">
                <p class="txtFazenda text-white">FAZENDA TCHISSOLA</p>
            </div>
            <div>
                <p class="txtFazendaP">PROVINCIA DA HUILA</p>
            </div>
            <div>
                <v-card-actions>
                    <ModalProdutoFazenda />
                </v-card-actions>
            </div>
        </div>

        <div class="filhoFazenda">
            <div class="imgFazenda4">
                <p class="txtFazenda text-white">FAZENDA MUMBA</p>
            </div>
            <div>
                <p class="txtFazendaP">PROVINCIA DA HUILA</p>
            </div>
            <div>
                <v-card-actions>
                    <ModalProdutoFazenda />
                </v-card-actions>
            </div>
        </div>
 
    </div>

    
</template>

<!-- Funcoes -->
  
 

<!-- Funcao Para abertura da modal -->

<!-- Fim da Funcao de abertura da -->

