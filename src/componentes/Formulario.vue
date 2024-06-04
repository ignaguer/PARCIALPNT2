<template>
  <section class="src-componentes-formulario">

    <h1>Parcial - PNT2</h1>
    
    <div class="form-group">
      <input
        id="texto"
        type="text"
        placeholder="Ingrese el texto"
        v-model.trim="texto"
      />
    </div>
    <p>Cantidad caracteres = {{ this.contarCaracteres }}</p>
    <div>1. - {{ this.cambiarVocales() }} - (codificado)</div>
    <div>2. - {{ texto.toUpperCase() }} - (mayuscula)</div>
    <div>3. - {{ texto.toLowerCase() }} - (minuscula)</div>
    <div>4. - {{ this.mayusculaMinuscula(texto) }} - (mayusculaMinuscula)</div>
    <div>5. - {{ this.minusculaMayuscula(texto) }} - (minusculaMayuscula)</div>


    <p>Respuestas: 1:C 2:C 3:A </p>
  </section>
</template>

<script lang="js">

export default  {
  name: 'src-componentes-formulario',
  props: [],
  mounted () {

  },
  data () {
    return {
      texto:''
    }
  },
  methods: {
     cambiarVocales(){
  let textoMin = this.texto.toLowerCase()
  let letra = ''
  for(let i = 0; i< textoMin.length; i++){
      switch(this.texto[i]){
          case 'a':
              letra += 'u';
              break;
          case 'e':
              letra += 'o';
              break;
          case 'o':
              letra += 'e';
              break;
          case 'u':
              letra += 'a';
              break;
          default:
              letra += this.texto[i];
      }
  }
  return letra;
 },
 mayusculaMinuscula(){
  let mayusculaMinuscula = ''
  for(let i = 0; i< this.texto.length; i++){
      if(i%2 == 0)
          mayusculaMinuscula += this.texto[i].toUpperCase()
      else
          mayusculaMinuscula += this.texto[i].toLowerCase()
  }
  return mayusculaMinuscula
 },
 minusculaMayuscula(){
  let minusculaMayuscula = ''
  for(let i = 0; i< this.texto.length; i++){
      if(i%2 == 0)
          minusculaMayuscula += this.texto[i].toLowerCase()
      else
          minusculaMayuscula += this.texto[i].toUpperCase()
  }
  return minusculaMayuscula
  }

  },
  computed: {
    contarCaracteres(){
      let cantidad = this.texto.length
      return cantidad
    },

    }

  }
</script>

<style scoped lang="css">
.src-componentes-formulario {
}
</style>
