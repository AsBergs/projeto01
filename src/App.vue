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
const usuario2 = ref(false);
const senhaErro = ref('');

function confirmasenha (){
  if(senha.value ==  senha2.value)
  senhaErro.value = "";
  return true;
}
   {
  senhaErro.value = "Você digitou duas senhas diferentes"
  return false;
}
</script>



