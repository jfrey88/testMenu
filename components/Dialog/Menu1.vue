<template>
    <v-dialog max-width="800">
  
      <template v-slot:default="{ isActive }">
        <v-card title="Envoyer bonjour à la console">
    
          <v-card-actions>
    
            <v-btn text="Non" @click="isActive.value = false"></v-btn>
            <v-btn text="Oui" @click="afficherBonjour()"></v-btn>
            
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
    const afficherBonjour =  () => {
      console.log("Bonjour");
  };
  