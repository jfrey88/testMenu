<template>
  <v-btn class="ma-3"  @click="ouvreMenu1()"> Menu 1 </v-btn>
  <v-btn class="ma-3" @click="ouvreMenu2()"> Menu 2 </v-btn>
  <v-btn class="ma-3" @click="ouvreMenu3()"> Menu 3 </v-btn>

  <DialogMenu1 v-model="dialogStatusMenu1" />
  <DialogMenu2 v-model="dialogStatusMenu2" />
  <DialogMenu3 
    v-model="dialogStatusMenu3" 
    @update:model-value="dialogStatusMenu3 = false" /> 
</template>


<script setup>

const dialogStatusMenu1 = ref(false);
const dialogStatusMenu2 = ref(false);
const dialogStatusMenu3 = ref(false);

const ouvreMenu1=()=>{
  console.log('je passe dans ouvreMenu1');
  dialogStatusMenu1.value=!dialogStatusMenu1.value;
}

const ouvreMenu2=()=>{
  console.log('je passe dans ouvreMenu2');
  dialogStatusMenu2.value=!dialogStatusMenu2.value;
}
const ouvreMenu3=()=>{
  console.log('je passe dans ouvreMenu3');
  dialogStatusMenu3.value=!dialogStatusMenu3.value;
}


</script>
