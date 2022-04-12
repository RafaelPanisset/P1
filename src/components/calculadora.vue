<template>
   <div>
       <h1> Calculadora </h1>
       <div>
            <input v-model="input1" placeholder="Primeiro valor">
            <input v-model="input2" placeholder="Segundo Valor">
       </div>
        <v-btn color="primary" @click="somar"> Soma </v-btn>
        <v-btn color="primary" @click="subtrair"> Subtração </v-btn>
        <v-btn color="primary" @click="multiplicar"> Multiplicação </v-btn>
        <v-btn color="primary" @click="dividir"> Divisão </v-btn>
   </div>
</template>

<script>


export default {
  name: "calculadora",
  data: () => ({
      input1:0,
      input2:0,
  }),
  methods: {
      somar() {
        var soma = this.input1 + this.input2;
        alert("Soma : ", soma);
      },
      subtrair() {
        var sub = this.input1 - this.input2;
        alert("Subtração : ", sub);
      },
  
      multiplicar() {
        var mult = this.input1 * this.input2;
        alert("Multiplicação  : ", mult);
      },
      dividir() {
            if (this.input2 == 0) {
                alert("Divisão por zero não é permitida!");
            }
            else {
                var div = this.input1 / this.input2;
                alert("Multiplicação  : ", div);
            }
      }
  },
 
};
</script>
