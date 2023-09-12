<template>
    <div>
        <div class="main">
            <div class="ctn" id="cadastro">
                <div id="ultimo_form" :class="!ultimo ? '' : 'fade'">
                    <table>
                        <tr>
                            <td><button class="btn" @click="toggleForm()"><v-icon>arrow_back</v-icon></button>
                            </td>
                            <td width="100%">
                                <h4>Preencha todos os campos</h4>
                            </td>
                        </tr>
                    </table><br>
                    <h1>Investidor</h1>
                    <p>Cadastre-se. como <b>Investidor.</b> e tenha acesso aos nossos e variados serviços</p><br>
                    <div id="formulario">
                        <input class="text-input" type="text" name="nome" placeholder="Nome completo" required>
                        <input class="text-input" type="email" name="email" placeholder="Insira o seu email" required>
                        <input class="text-input" type="password" name="senha" placeholder="Insira a sua senha" required>
                        <input class="text-input" type="number" name="telefone" placeholder="Nº telefone" required>
                        <input class="text-input" type="email" name="email" placeholder="Insira o seu email" required>
                        <input class="text-input" type="text" name="bi" placeholder="Bilhete de identidade" required>
                        <input class="text-input" type="date" name="nascimento" placeholder="Data de nascimento">
                    </div>
                    <small>Fique a apar das nossas novidades, consulte os nossos <a href="#">termos e condições</a> para
                            uma
                            utilização opyimizada.</small><br><br>
                        <input class="c-sia-1 btn" @click="toggleFadCad()" type="submit" value="Continuar">
                </div>
                <div id="fade-cad" :class="!fade ? '' : 'right'">
                    <div id="fazendeiro">
                        <table cellspacing="0">
                            <tr>
                            <tr>
                                <td><button class="btn" @click="toggleFadCad()">
                                        <v-icon>arrow_back</v-icon></button></td>
                                <td >
                                    <h4>Selecione uma das opcções</h4>
                                </td>
                            </tr>
                            <td colspan="2" height="100%" style="padding-bottom: 70px;"  @click="toggleForm()">
                                <button class="card-select-cad">
                                    <div class="card-select-icon"><v-icon>agriculture</v-icon></div>
                                    <div class="card-select-title">
                                        <h2>fazendeiro</h2>
                                    </div>
                                    <div class="card-select-footer">rodape</div>
                                </button>
                            </td>
                            </tr>
                        </table>
                    </div>
                </div>
                <div id="campos" action="#" :class="!campos ? '' : 'fade'">
                    <h1>Cadastra-se</h1><br><br>
                    <p>Cadastre-se. como <b>cadastro.</b> e tenha acesso aos nossos e variados serviços</p><br>
                    <input class="text-input" type="text" name="nome" placeholder="Nome completo" required>
                    <input class="text-input" type="email" name="email" placeholder="Insira o seu email" required>
                    <input class="text-input" type="password" name="senha" placeholder="Insira a sua senha" required>
                    <input class="text-input" type="number" name="telefone" placeholder="Nº telefone" required>
                    <input class="text-input" type="email" name="email" placeholder="Insira o seu email" required>
                    <input class="text-input" type="text" name="bi" placeholder="Bilhete de identidade" required>
                    <input class="text-input" type="date" name="nascimento" placeholder="Data de nascimento">
                    <small>Fique a apar das nossas novidades, consulte os nossos <a href="#">termos e condições</a> para uma
                        utilização opyimizada.</small><br><br>
                    <input class="c-sia-1 btn" @click="toggleFadCad()" type="submit" value="Continuar">
                </div>
                <div id="investidor" action="#">
                    <table>
                        <tr>
                            <td heigth="100%">
                                <button class="card-select-cad" @click="toggleForm()">
                                    <div class="card-select-icon"><v-icon>attach_money</v-icon></div>
                                    <div class="card-select-title">
                                        <h2>Investidor</h2>
                                    </div>
                                    <div class="card-select-footer">rodape</div>
                                </button>
                            </td>
                        </tr>
                    </table>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import '~/assets/css/main.sass'
import Swal from "sweetalert2";
import '~/assets/css/perfil.scss'
import '~/assets/css/menu.scss'

definePageMeta({
    layout: false,
});

export default {
    data: () => ({
        campos: false,
        fade: false,
        ultimo: false
    }),
    methods: {
        toggleFadCad() {
            this.campos = !this.campos
            this.fade = !this.fade
        },
        toggleForm() {
            this.ultimo = !this.ultimo
        }
    }
}
</script>

<style>

#formulario{
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 10px;
}

#cadastro {
    display: flex;
    position: fixed;
    width: 100%;
    height: 100%;
    max-height: 500px;
    max-width: 900px;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    margin: auto;
    overflow: hidden;
    padding: 60px 10px;
}

#cadastro div {
    overflow: auto;
    max-height: 100%;
}

#campos,
#investidor {
    padding: 0 30px;
    width: 50%;
    max-width: 50%;
    min-height: 50%;
}

#campos {
    transition: .4s;
}

#campos.fade {
    opacity: 0;
}

#fade-cad {
    z-index: 100;
    transition: .4s;
    position: absolute;
    width: 50%;
    height: 100%;
    background-color: #fff;
    top: 0;
    right: 0;
    overflow: hidden;
}

#fade-cad::before {
    transition: .4s;
    position: absolute;
    background-image: url("/img/4.jpg");
    content: "  ";
    display: flex;
    width: 100%;
    height: inherit;
    background-position: center;
    background-size: cover;
    top: 0;
    left: 0;
}

#fazendeiro {
    transition: .4s;
    position: absolute;
    background-color: #fff;
    height: 100%;
    width: 100%;
    right: 100%;
}

#fade-cad.right {
    right: 50% !important;
}

#fade-cad.right #fazendeiro {
    right: 0 !important;

}

/* #fade-cad.right::before {} */

.card-select-cad {
    display: block;
    width: 100%;
    max-width: 200px;
    margin: auto;
    text-align: center;
    padding: 20px;
    border-radius: 10px;
    border: 4px solid #ddd;
}

.card-select-icon {
    transition: .4s;
    padding: 40px;
    background-color: #ddd;
    border-radius: 10px;
    width: calc(100% - 80px);
    border: none;
    margin-bottom: 15px;
}

#fazendeiro .card-select-cad:hover {
    border-color: #1d9e1d !important;
}

#investidor .card-select-cad:hover {
    border-color: #2444ae !important;
}

#fazendeiro .card-select-cad:hover .card-select-icon {
    background-color: #1d9e1d !important;
}

#investidor .card-select-cad:hover .card-select-icon {
    background-color: #2444ae !important;
}

.card-select-cad:hover .card-select-icon {
    transform: scale(1.08);
}

.card-select-cad:hover .card-select-icon i {
    color: white;
}

.card-select-icon i {
    font-size: 24pt;
}

#fazendeiro table,
#investidor table {
    width: 100%;
    height: 100%;
}

#ultimo_form {
    display: none;
    opacity: 0;
    box-sizing: border-box;
    background-color: white;
    position: absolute;
    top: 0;
    left: 0;
    z-index: 101;
    width: 100%;
    height: 100%;
    padding: 20px;
    overflow: auto;
}

#ultimo_form.fade {
    display: block;
    opacity: 1;
}
</style>