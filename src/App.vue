<script setup>
import { ref } from 'vue'

const nome = ref('');
const email = ref('');
const senha = ref('');
const senhaConfirma = ref('');
const dataNasc = ref('');
const endereço = ref('');
const cidade = ref('');
const estado = ref('');
const hobbies = ref('');
const lingprog = ref('');
const biografia = ref('');
const confirmarUsuario = ref(false);
const senhaErro = ref('');

function confirmasenha() {
  if (senha.value == senhaConfirma.value)
    senhaErro.value = ""
  return true;

}


</script>
<template>
  <div class="div1">
    <form @submit.prevent="confirmarUsuario = confirmasenha()" class="formulario">
      <div class="menu">
        <p>Nome: </p><input v-model="nome" placeholder="Nome" minlength="3" maxlength="20" required />
        <p>Email: </p><input type="email" v-model="email" placeholder="Email" required />
        <p>Senha: </p><input type="password" v-model="senha" required />
        <p>Confirmação de senha: </p><input type="password" v-model="senhaConfirma" required />
        <p>Nascimento: </p><input type="date" name="Data nascimento" id="dataNasc" v-model="dataNasc">
        <p>Endereço: </p><input type="text" v-model="endereço" required />
        <p>Cidade: </p><input type="text" v-model="cidade" required />


        <p>Estado: </p><select v-model="estado">
          <option value=" Acre">AC</option>
          <option value="Alagoas">AL</option>
          <option value="Amapá">AP</option>
          <option value="Amazonas">AM</option>
          <option value="Bahia">BA</option>
          <option value="Ceará">CE</option>
          <option value="Distrito Federal">DF</option>
          <option value="Espírito Santo">ES</option>
          <option value="Goiás">GO</option>
          <option value="Maranhão">MA</option>
          <option value="Mato Grosso">MT</option>
          <option value="Mato Grosso do Sul">MS</option>
          <option value="Minas Gerais">MG</option>
          <option value="Pará">PA</option>
          <option value="Paraíba">PB</option>
          <option value="Paraná">PR</option>
          <option value="Pernambuco">PE</option>
          <option value="Piauí">PI</option>
          <option value="Rio de Janeiro">RJ</option>
          <option value="Rio Grande do Norte">RN</option>
          <option value="Rio Grande do Sul">RS</option>
          <option value="Rondônia">RO</option>
          <option value="Roraima">RR</option>
          <option value="Santa Catarina">SC</option>
          <option value="São Paulo">SP</option>
          <option value="Sergipe">SE</option>
          <option value="Tocantins">TO</option>
        </select>
        <p>Hobbies: </p><textarea v-model="hobbies" cols="20" rows="5"></textarea>
        <p>Linguagens de programação: </p><textarea v-model="lingprog" cols="20" rows="5"></textarea>
        <p>Biografia: </p><textarea v-model="biografia" cols="20" rows="5"></textarea>
        <button type="submit" class="button">Enviar</button>
        <p>{{ senhaErro }}</p>
      </div>
    </form>

    <div v-if="confirmarUsuario" class="formulario2">

      <div class="usuario">
        <p>Usúario</p>
        <p>Nome: {{ nome }}</p>
        <p>Email: {{ email }}</p>
        <p>Senha: {{ senha }}</p>
        <p>Data de nascimento: {{ dataNasc }}</p>
        <p>Endereço: {{ endereço }}</p>
        <p>Cidade: {{ cidade }}</p>
        <p>Estado: {{ estado }}</p>
        <p>Hobbies: {{ hobbies }}</p>
        <p>Linguagens de programação: {{ lingprog }}</p>
        <p>Biografia: {{ biografia }}</p>
      </div>

    </div>

  </div>
</template>
<style scoped>
.formulario {
  color: rgb(115, 184, 245);
  background-color: #0E4459;
  width: 350px;
  border-radius: 20px;
 margin-left: 20%;
}

.formulario2 {
  color: rgb(144, 196, 242);
  background-color: #0E4459;
  border-radius: 20px;
 margin-right: 30px;

  margin-left: 130px;
}

.menu {
  margin: 50px 50px 50px 90px;

}

.button {
  font-size: 15px;
  color: rgb(152, 201, 244);
  background-color: #07748d;
  border: solid 1px #3d43e9;
  border-radius: 20px;
  margin: 20px 10px 10px 0px
}

.div1 {
  display: grid;
  grid-template-columns: 50% 50%;
}


.usuario {
  color: rgb(12, 217, 245);
  background-color: #0E4459;
 margin-top: 10%;
 margin-left: 10%;
 margin-right: 10%;

}
</style>



