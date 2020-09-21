<template>
    <div class="conversor">
        <h2 class="display-3">Bin2Dec</h2>
        <input type="number" id="campo-numero" v-model='entrada' placeholder="Seu número binário aqui">
        <button id="botao-converter" class = "btn btn-primary" @click="converter(numeroBinario(entrada))"><i class="fas fa-exchange-alt"></i></button>
        <h3 id="numero-convertido">Resultado: {{numero}}</h3>
    </div>
</template>

<script>
export default {
    name: 'bin-2-dec',
    data() {
        return {
            entrada: '',
            numero : 0
        }
    },
    methods: {
        numeroBinario(texto) {
            var numeroBin = texto.split('');
            return numeroBin;
        },
        converter(binario){
            binario.reverse();
            var decimal = 0;
            for (var i = 0; i < binario.length; i++) {
                decimal = decimal + (binario[i] * Math.pow(2, i));
            
            }
            this.numero = decimal;
        }
    }
}
</script>
