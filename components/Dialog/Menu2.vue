<template>
    <v-dialog max-width="800">
  
      <template v-slot:default="{ isActive }">
        <v-card title="Envoyer bonsoir à la console">
    
          <v-card-actions>
    
            <v-btn text="Non" @click="isActive.value = false"></v-btn>
            <v-btn text="Oui" @click="afficherBonsoir()"></v-btn>
            
          </v-card-actions>
        </v-card>
      </template>
    </v-dialog>
  </template>
  <script setup>
  import { defineProps} from "vue";
    const props = defineProps({
      isCreate: Boolean,
    });

    const emit = defineEmits(["update:modelValue"]);
    const afficherBonsoir =  () => {
      console.log("Bonsoir",props);
      emit("update:modelValue");
  };
  
</script>
  