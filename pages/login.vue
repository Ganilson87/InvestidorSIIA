<template>
  <div>
    <div id="login" class="ctn">
      <form action="#">
        <h3>SIIA</h3> <br>
        <h1>Faça Login</h1>
        <p>Prencha os campos abaixo para fazer o login.</p><br>
        <input v-model="email" type="text" name="email" placeholder="Insira o seu email" class="text-input" required>
        <input v-model="password" type="password" name="senha" placeholder="Insira a sua senha" class="text-input" required><br><br>
        <small>Fique a apar das nossas novidades, consulte os nossos <a href="#">termos e condições</a> para uma
          utilização opyimizada.</small><br><br>
        <input class="primary btn" type="button" value="Entrar" @click="login()">
        <NuxtLink to="/cadastro" class="btn second">Cadastre-se</NuxtLink>
      </form>
    </div>
  </div>
</template>

<script>
import Swal from 'sweetalert2';
//import auth from '~/services/auth.js';
import '~/assets/css/perfil.scss'
import '~/assets/css/menu.scss'

definePageMeta({
  layout: false,
});
export default {
  data() {
    return {
      email: '',
      password: '',
    };
  },

  methods: {
    async login() {
      try {
        if (!this.nome && !this.email) {
          Swal.fire(
            'Preencha todos os campos',
            'Nome do usuario ou palavra-passe inseridos incorretamento, Tente novamente',
            'question'
          )
          return
        }
        await auth.login(this.email, this.password);
        this.$router.push('/'); // redireciona para a página inicial após o login
      } catch (error) {
        Swal.fire(
          'Informações incorretas',
          'Nome do usuario ou palavra-passe inseridos incorretamento, Tente novamente',
          'question'
        )
      }
    },
  },
};
</script>
<style>
#login {
  position: fixed;
  width: 100%;
  height: 100%;
  max-height: 550px;
  max-width: 500px;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  margin: auto;
  padding: 50px;
}
</style>
