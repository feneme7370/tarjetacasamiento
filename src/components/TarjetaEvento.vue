<script setup>
    const props = defineProps({
        nombre: {type: String, required: true},
        fecha: {type: String, required: true},
        lugar: {type: String, required: true},
        imagen: {type: String, required: true},
        mapa: {type: String, required: true},
    })
</script>

<template>
    <div class="max-w-md mx-auto bg-emerald-50 rounded-md shadow-md overflow-hidden my-4 ">
        <img :src=" imagen  " alt="Evento 1" class="w-full h-60 object-cover">
        <div class="p-4">
            <h2 class="text-2xl font-bold mb-2 cursiva">{{ nombre }}</h2>
            <p class="text-xl mb-2">{{ fecha }}</p>
            <p class="text-xl mb-2">{{ lugar }}</p>
            <div class="mt-1 flex justify-center items-center">
                <a :href=" mapa " target="_blank" class="bg-emerald-700 hover:bg-emerald-800 text-white text-lg py-1 px-2 rounded focus:outline-none focus:shadow-outline text-center">Ver en Mapa</a>
            </div>
        </div>
    </div>
</template>

<style scoped>

</style>