<script setup>
import { ref } from 'vue'

const appName = ref('Ta Galerie')
var imageCompter = 0

const newUrl = ref('')
const images = ref([])

function ajouterImage() {
  if (newUrl.value === '') {
    return
  }

  images.value.push(newUrl.value)
  newUrl.value = ''
  imageCompter = imageCompter + 1
}


</script>

<template>
  <h1>{{ appName }}</h1>

  <input type="text" v-model="newUrl" placeholder="Entrez l'URL d'une image" />
  <button @click="ajouterImage">Ajouter</button>

  <h2>Total d'images : {{ imageCompter }}</h2>

  <p>Aucune image ajoutée</p>

  <div v-for="image in images">
    <img :src="image" width="150" />
  </div>

</template>

<style scoped></style>
