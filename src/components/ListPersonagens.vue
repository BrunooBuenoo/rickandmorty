<script setup>
    const personagem = defineProps(["name", "url", "status", "species", "gender", "location", "image" , "episode"])
    
</script>

<template>
    <div class="col-md-4">
        <div class="card mb-3 p-5"  style="max-height: 700px; min-height: 700px;">
            <img :src="personagem.image" class="card-img-top" height="100%" alt="...">
            <div class="card-body">
                <p class="card-title">Nome: {{ personagem.name }}</p>
                <p class="card-title">Status: 
                    <font v-if="personagem.status === 'Alive'" color="green">{{ personagem.status }}</font>
                    <font v-else-if="personagem.status === 'unknown' "color="yellow">{{ personagem.status }}</font>
                    <font v-else color="red">{{ personagem.status }}</font>
                </p>
                <p class="card-title">Espécie: {{ personagem.species }}</p>
                <p class="card-title">Gênero: {{ personagem.gender }}</p>
                <p class="card-title">Localização: {{ personagem.location.name }}</p>
                <p class="card-title">Aparece em 
                    <font v-if="personagem.status === 'Alive'" color="green" style="font-size: 25px">{{ personagem.episode.length }}</font>
                    <font v-else-if="personagem.status === 'unknown' "color="yellow" style="font-size: 25px">{{ personagem.episode.length }}</font>
                    <font v-else color="red" style="font-size: 20px">{{ personagem.episode.length }}</font> episódios </p>
            </div>
        </div>

    </div>
</template>

<style>

</style>