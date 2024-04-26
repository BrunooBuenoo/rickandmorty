<script setup>
import {ref} from 'vue'

let num = ref(0)

</script>

<template>
  <!-- Menu Bootstrap-->

  <nav class="navbar navbar-expand-lg navbar-dark border-bottom border-body">
  <div class="container-fluid">
    <!-- <a class="navbar-brand" href="#">Pokedex</a> -->
    <router-link class="navbar-brand" to="/">Rick and Morty</router-link>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item">
          <!-- <a class="nav-link" href="#">Sobre</a> -->
          <router-link class="nav-link" to="/about">Sobre</router-link>
        </li>
      </ul>
    </div>
  </div>
</nav>

<div class="main">
  <RouterView></RouterView>
</div>

<footer class="bg-dark text-light">
  <div>
    Unimar | ADS | {{ new Date().getDate() }} - {{ new Date().getDay() }} - {{ new Date().getFullYear() }}
  </div>
</footer>

</template>
<style>
body{
  background-image: url(https://img.elo7.com.br/product/zoom/3BAB0FA/papel-de-parede-rick-and-morty-dc.jpg);
}

footer{
  position: fixed;
  bottom: 0;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 40px;
}

.about {
  width: 100%;
  height: 90vh;
  background-color:#011b37;
  color: white;
}

.about img.eu{
  width: 220px;
  height: 220px;
  border-radius: 50%;
  border: 3px solid #ffffff;
}

.persons img.rm{
  margin-top: 10vh;
  margin-left: 30%;
  width: 10vw;
}

.persons img.escrita{
  margin-top: 10vh;
  margin-left: 1vh;
  width: 30vw;
}


.apresentacao {
  padding-left: 30vw;
  padding-top: 10vh;
  display: flex;
}

.info{
  padding-left: 2vw;
  padding-top: 4vh;
}
</style>