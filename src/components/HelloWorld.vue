<template>
  <div class="hello">
    
    <h1>{{ msg }} </h1>
    <p>{{ ola }}</p>
    <p v-if="booleano"><input v-model = "nome" placeholder="Nome: "/></p>
    <p id="nome">Bem vindo {{ nome }}</p>
    <h1>Contador: {{ contador }}</h1>
    <p v-if = "visualizar">{{ viu }}</p>

    <button @click="ver">Ocultar</button>
    <button @click="retangulo">Ocultar o campo Nome</button>
    <button @click="incrementar">Incrementar</button>
    <button @click="decrementar">Decrementar</button>

  </div>
  <ul>
    <li v-for="item in a" :key="item.text">
      {{ item.text }}
    </li>
  </ul>
  <p id="verde">Lorem ipsum dolor sit amet consectetur adipisicing elit. Nostrum reprehenderit facere aut? Praesentium nam dolor, earum alias omnis doloribus ducimus ex adipisci saepe laboriosam numquam sequi magni, est natus blanditiis.</p>
</template>

<script>
export default {
  data(){
    return {
      ola: 'Bem Vindo ao Vue.js',
      contador: 0,
      visualizar: false,
      booleano: true,
      viu: "Visualizar?",
      a:[
        {text: "Eduardo"},
        {text: "Gabriel"},
        {text: "Gabis"},
        {text:"SeiLaEU"}
        ],
        nome:""
    }
  },
  methods:{
incrementar(){
this.contador++;
},
decrementar(){
  this.contador--;
},
ver(){
  this.visualizar = !this.visualizar
},
retangulo(){
  this.booleano = !this.booleano
}
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}

a {
  color: #42b983;
}
#verde{
  color: #42b983;
}
</style>
