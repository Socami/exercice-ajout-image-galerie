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

  <input class="champ" type="text" v-model="newUrl" placeholder="Entrez l'URL d'une image" />
  <button class="add-button" @click="ajouterImage">Ajouter</button>

  <h2>Total d'images : {{ imageCompter }}</h2>

  <p>Aucune image ajoutée</p>
<div class="images">
    <div v-for="image in images">
    <img :src="image" width="150" />
  </div>
</div>


</template>

<style scoped>
img{
  border-radius: 10px;
}
.images{
  display: flex;
  gap: 10px;
}
h1,h2,p{
  font-family: Arial, Helvetica, sans-serif;
}

body{
  background-color: black;
  color: white;
}

.champ{
  height: 20px;
  border: solid 1px gray;
  border-radius: 6px 0 0 6px;
}

.add-button{
  height: 24px;
  background-color: rgb(255, 191, 0);
  color: balck;
  border: none;
  border-radius: 0 6px 6px 0;
  font-weight: bold;
}
</style>

<style>
  body{
    background-color: black;
    color: white;
  }
</style>
