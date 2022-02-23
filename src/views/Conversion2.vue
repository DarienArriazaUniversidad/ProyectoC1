<template lang="html">

<div class="conversion2">
    <h1>pagina 2----</h1>
  
  <section class="conversion2">
    <b-card bg-variant="warning">
    <b-form-group
      label-cols-lg="3"
      label="Conversor de monedas"
      label-size="lg"
      label-class="font-weight-bold pt-0"
      class="mb-0"
      >
      <b-form-group
        label="Primer Valor:"
        label-for="n1"
        label-cols-sm="3"
        label-align-sm="right"
        >
        <!--  -->
        <b-form-input v-model="data" type="number"></b-form-input>
      </b-form-group>
        <b-form-group
          label="Conversion a:"
          label-cols-sm="3"
          label-align-sm="right"
          class="mb-0">

          <b-form-select v-model="selectedValue">            
            <b-form-select-option value="">Por favor seleccione una opcion</b-form-select-option>
            <b-form-select-option  value="1">Dolar a Euro</b-form-select-option>
            <b-form-select-option id="opB"  value="2">Euro a Dolar</b-form-select-option>
              <b-form-select-option id="opC"  value="3">Colon a Dolar</b-form-select-option>
              <b-form-select-option id="opD"  value="4">Dolar a Colon</b-form-select-option>
              <b-form-select-option id="opE"  value="5">Libra Esterlina a Dolar</b-form-select-option>
                
          </b-form-select>
          <hr>
          <!--  -->
          <b-button @click="calcular()" variant="dark" size="lg" class="pt-2">Convertir a</b-button>
        </b-form-group>
    </b-form-group>
  </b-card>
  </section>

</div>
</template>

<script lang="js">
  export default  {
    name: 'conversion2',
    data(){ 
       return {
        selectedValue: 0,
        data:0
     }
    },
    methods: {
      calcular(){        
        let val = this.selectedValue;
        let result=0;
        let results="";
        if(val ==1){
          result= this.data *0.8252;
          results= "El resultado de la conversion DOlar a Euro de "+ val+" es: "+result;
        }
        if(val==2){
          result=this.data*1.2118
        }
        return alert(results) //solo se define un return en la funcion
      }
    }
  }
  </script>
      /*
      console.log(comparar);
      if (comparar == 'a')
      {
        var dolar = this.data2;
        var euro = 0.8252;
        var operacionB = (dolar * euro).toFixed(2);
        alert('El resultado fue: '+ operacionB)
        
      }
       else if (comparar == 'b')  
      {
        var euro1 = this.data2;
        var dolar1 = 1.2118;
        var operacion1B = (euro1*dolar1).toFixed(2); 
        alert('El resultado es: ' + operacion1B)
      }
      else if (comparar == 'c')
      {
        var colon = this.data2;
        var dolar2 = 0.1141;
        var operacion2B = (colon*dolar2).toFixed(2);
        alert('El resultado es: ' + operacion2B)
      }
      else if (comparar == 'd')
      {
          var dolar3 = this.data2;
          var colon1 = 8.7653;
          var operacion3B = (dolar3*colon1).toFixed(2);
          alert('El resultado es: ' + operacion3B) 
      }
      else if (comparar == 'e')
      {
          var dolar4 = this.data2;
          var libra = 1.4016;
          var operacion4B = (dolar4*libra).toFixed(2);
          alert('El resultado es: ' + operacion4B) 
      }
      else 
      {
        alert('Seleccione una opcion por favor!')
      }
       

      }
*/
    