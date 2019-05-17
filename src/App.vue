<template>
<div class="container">
<div class="row">
            <div class="col-xs-12">
             <h2> Colors </h2>
           <button class="blue" @click="selectedComponent = 'AppBlue'">Blue</button>
           <button class="red" @click="selectedComponent = 'AppRed'">Red</button>
           <button class="green" @click ="selectedComponent = 'AppGreen'">Green</button>
           <hr>
           <p> {{ selectedComponent }} </p>
           <component :is="selectedComponent"> 
          </component>
   
             
            </div>
        </div>

</div>
</template>

<script>

import Blue from './components/Blue.vue';
import Green from './components/Green.vue';
import Red from './components/Red.vue';

export default{
  data: function(){
    return {
      selectedComponent: 'AppBlue'
    }
  },

  components: {
    AppBlue: Blue,
    AppRed: Red,
    AppGreen: Green,
  
  }
}

</script>

<style scoped>

div {

      
        padding: 40px;
        margin: 40px auto;
        text-align: center;
        background-color: white;

}
h2{
    color: #660066;
    text-align: center;
}

.blue{
  background-color: #3333ff;
   border: 1px solid #0066ff;
}

.red{
  background-color: #ff0000;
   border: 1px solid red;
}

.green{
  background-color: #00cc00;
   border: 1px solid green;
}

button {
  color: white;
}


</style>
