<template>
    <v-dialog max-width="800">
  
      <template v-slot:default="{ isActive }">
        <v-card title="Envoyer bonne journée à la console">
    
          <v-card-actions>
    
            <v-btn text="Non" @click="emit('update:modelValue', false)"></v-btn>
            <v-btn text="Oui" @click="afficherBonnejournee()"></v-btn>
            
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

    const afficherBonnejournee =  () => {
      console.log("Bonne journée");
      emit("update:modelValue", false);
  };
</script>