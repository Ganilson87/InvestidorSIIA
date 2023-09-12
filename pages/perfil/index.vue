<template>
  <div id="perfil">
    <div id="perfil-resumo">
      <div id="info" class="ctn">
        <div id="foto-capa"></div>
        <div id="foto-perfil"></div>
        <div style="padding-top: 70px; text-align: center;">
          <h1 id="nome-usuario">{{ user.first_name }} {{ user.last_name }}</h1>
          <small>{{ user.email }}</small><br>
          <button class="btn-round c-sia-1">Botão de acção</button>
        </div>
      </div>
      <div class="ctn">
        <table>
          <tr>
            <td><v-icon>star</v-icon></td>
            <td width="100%">
              <h4>Detalhes</h4>
            </td>
            <td><button style="background-color: #ddd; padding: 15px; border-radius: 50%;" class="btn">
                <v-icon>arrow_forward</v-icon></button></td>
          </tr>
        </table>
        <div class="sia-card-1">
          <table>
            <tr>
              <td rowspan="2">
                <div class="icon-notf"></div>
              </td>
              <td style="vertical-align: bottom;">
                <h2 class="title">Noticia</h2>
              </td>
            </tr>
            <tr>
              <td style="vertical-align: top;">
                <p class="desc">Breve descrição...</p>
              </td>
            </tr>
          </table>
        </div>
      </div>
      <div class="ctn">
        <table>
          <tr>
            <td><v-icon>info</v-icon></td>
            <td width="100%">
              <h4>Detalhes</h4>
            </td>
            <td><button style="background-color: #ddd; padding: 15px; border-radius: 50%;" class="btn">
                <v-icon>edit</v-icon></button></td>
          </tr>
        </table>
        <div id="dados-usuario">
          <table>
            <tr>
              <td>
                <h3>Nome</h3>
              </td>
              <td><span>{{ user.first_name }} {{ user.last_name }}</span></td>
            </tr>
            <tr>
              <td>
                <h3>Email</h3>
              </td>
              <td><span>{{ user.email }}</span></td>
            </tr>
            <tr>
              <td>
                <h3>Bi</h3>
              </td>
              <td><span>{{ user.bi }}</span></td>
            </tr>
            <tr>
              <td>
                <h3>Endereço</h3>
              </td>
              <td><span>{{ user.endereco1 }}</span></td>
            </tr>
            <tr>
              <td>
                <h3>Telefone</h3>
              </td>
              <td><span>{{ user.Telefone }}</span></td>
            </tr>
          </table>
        </div>
      </div>
    </div>
    <div id="feed-perfil">
      <table>
        <tr>
          <td><v-icon>money</v-icon></td>
          <td width="100%">
            <h4>Carteira</h4>
          </td>
        </tr>
      </table>
      <div id="meu-cartao">
        <table style="margin-bottom: 160px;">
          <tr>
            <td width="100%"><img src="/logo-white-icon.png" width="120"></td>
            <td>
              <pre class="text-white">Cartão digital</pre>
            </td>
          </tr>
        </table>
        <div class="sia-card-1">
          <table> 
            <tr>
              <td rowspan="4">
                <div id="imgChip"></div>
              </td>
              <td width="100%" style="vertical-align: bottom;">
                <h2 class="title">1234 5678 9101</h2>
              </td>
              <td style="text-align: center; vertical-align: bottom;">
                <pre>Saldo Disponivél</pre>
              </td>
            </tr>
            <tr>
              <td style="vertical-align: top;">
                <p class="desc text-white">{{ user.first_name }} {{ user.last_name }}</p>
              </td>
              <td style="vertical-align: super;text-align: right;">
                <pre><small><b>{{ (Number(user.saldo)).toLocaleString('pt-br') }}Kz</b></small></pre>
              </td>
            </tr>
          </table>
        </div>
      </div>
      <div class="ctn">
        <table>
          <tr>
            <td><v-icon>info</v-icon></td>
            <td width="100%">
              <h4>Historico</h4>
            </td>
          </tr>
        </table>
        <div id="dados-usuario">
          <br>
          <table>
            <tr v-for="historico, index in historicos" :key="index">
              <td>
                <h3>{{ historico.descricao }}</h3>
                <p> <v-icon :style="corEstado(historico.estado)">{{ historico.estado === "mais" ? "add" : "remove" }}</v-icon> {{(historico.valor).toLocaleString('pt-br') }}Kz</p>
              </td>
              <td><span>{{ historico.data }}</span></td>
            </tr>
            
          </table>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import "~/assets/css/perfil.scss"
//import usuario from "~/services/usuario";

export default {
  mounted() {
   // this.dadosUser()
  },
  data: () => ({
    user: {},
    historicos: [
      {
        descricao: "Venda de Batata",
        estado: "mais",
        data: "01 de Agosto de 2023",
        valor: 535000
      },
      {
        descricao: "Venda de Tomate",
        estado: "mais",
        data: "04 de Julho de 2023",
        valor: 810000
      },
      {
        descricao: "Pagamento de Máquinas",
        estado: "menos",
        data: "19 de Junho de 2023",
        valor: 350000
      },
      {
        descricao: "Venda de Peras",
        estado: "mais",
        data: "03 de Junho de 2023",
        valor: 105000
      },
      {
        descricao: "Investimento na Fazenda Mumba",
        estado: "menos",
        data: "01 de Maio de 2023",
        valor: 700000
      },
      {
        descricao: "Pagamento de Adubos",
        estado: "menos",
        data: "30 de Abril de 2023",
        valor: 350000
      },
    ]
  }),
  methods: {
    corEstado(estado){
      if(estado === "mais"){
        return `color: green; font-size: 16px;`
      }else{
        return `color: red; font-size: 16px;`
      }
    },

    async dadosUser() {
      // if (process.browser) {
     // const userJSON = localStorage.getItem('user');
      //const userObj = JSON.parse(userJSON);
      //this.user = userObj
      //if (!userObj) {
       // return navigateTo('/login')
      //} else {
        //await usuario.getMe(userObj.id).then((response) => {
          //console.log(response)
        //   this.user = response
        // })
      // }

    }
  }

}
</script>