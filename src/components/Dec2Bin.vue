<template>
    <div class="conversor">
        <h2 class="display-3">Dec2Bin</h2>
        <input type="number" id="campo-numero" placeholder="Seu número decimal aqui" v-model="entrada">
        <button id="botao-converter" class = "btn btn-primary" @click="converter(entrada)"><i class="fas fa-exchange-alt"></i></button>
        <h3 id="numero-convertido">Resultado: {{saida}}</h3>
    </div>
    
</template>

<script>
export default {
    data() {
        return{
            entrada: '',
            saida: '0'
        }
    },
    methods: {
        converter(decimal) {
            var binString = '';
            while (parseInt(decimal) > 0) {
                binString = (decimal%2) +''+ binString;
                decimal = Math.floor(decimal/2);

            }
            this.saida = binString;
        }
    }
    
}
</script>
