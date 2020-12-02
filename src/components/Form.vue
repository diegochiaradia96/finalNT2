<template>
<div class="jumbotron">

    <form novalidate autocomplete="off" class="p-3 mt-3 text-left" >
      <div class="form-group col-4">
          <label for="texto"><h4>Color:</h4></label>
          <input 
            type="text"
            id="nombre"
            class="form-control"
            v-model="color"
          >
          </div>
          <div class="form-group col-4">
          <label for="texto"><h4>Fondo:</h4></label>
          <input 
            type="text"
            id="nombre"
            class="form-control"
            v-model="fondo"
          >
          </div>
          <div class="form-group col-4">
          <label for="texto"><h4>Size: </h4></label>
          <input 
            type="text"
            id="nombre"
            class="form-control"
            v-model="tamanio"
          >
          </div>
       <div class="form-group col-4"  >
          <label for="texto"  ><h4>texto </h4></label>
          <input :style="{ color: color, fontSize: tamanio + 'px', backgroundColor: fondo}"
            type="text"
            id="nombre"
            class="form-control"
            v-model="text"
          >
          </div>
     
       <h2>cantidad de palabras: {{cantidadDePalabras}}</h2>

     <br><br>
    <h2>Choice</h2>
      <p>pregunta: 1, respuestas: ['b']</p>
         <p> pregunta: 2, respuestas: ['c']</p>
         <p> pregunta: 3, respuestas: ['a','b']</p>
         <p> pregunta: 4, respuestas: ['c']</p>
         <p> pregunta: 5, respuestas: ['a','d']</p>
           
    </form>
 
</div>
</template>

<script>



  
  
  export default  {
    name: 'src-components-form',
    props: [],
   
    mounted () {

    },
    data () {
      return {
       text: '', 
       color: '',
       tamanio: '',
       fondo: ''
      }
    },
     
   
    methods: {
    
    },
    computed: {
   
   cantidadDePalabras(){
     let number
     if (this.text === '') {
       number = 0
     }
     else {
     
     let array = this.text.split(' ')
     number = array.length
      }
     return number
   }
   
   
   }
    
}


</script>

<style scoped lang="css">
  .src-components-form {

  }

  
</style>
