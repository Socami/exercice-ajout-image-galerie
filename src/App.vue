<script setup>
import { ref } from 'vue'

const appName = ref('Ta Galery')
const totalImage = 0

const newUrl = ref('')
const images = ref([])

function ajouterImage() {
  images.value.push(newUrl.value)
  newUrl.value = ''
}


</script>

<template>
  <h1>{{ appName }}</h1>

  <input type="text" placeholder="Entrez l'URL d'une image" />
  <button>Ajouter</button>

  <h2>Total d'images : {{ totalImage }}</h2>

  <p>Aucune image ajoutée</p>
</template>

<style scoped></style>
