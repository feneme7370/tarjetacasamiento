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
    <div class="max-w-md mx-auto bg-white rounded-md shadow-md overflow-hidden my-4 cursiva">
        <img :src=" imagen  " alt="Evento 1" class="w-full h-60 object-cover">
        <div class="p-4 font-bold">
            <h2 class="text-4xl font-bold mb-2 cursiva">{{ nombre }}</h2>
            <p class="text-2xl mb-2">{{ fecha }}</p>
            <p class="text-2xl mb-2">{{ lugar }}</p>
            <div class="mt-1 flex justify-center items-center">
                <a :href=" mapa " target="_blank" class="fondo-primario hover:fondo-primario-dark text-white text-2xl py-1 px-2 rounded focus:outline-none focus:shadow-outline text-center flex items-center justify-center gap-3">
                    <span>
                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M15 10.5a3 3 0 11-6 0 3 3 0 016 0z" />
                        <path stroke-linecap="round" stroke-linejoin="round" d="M19.5 10.5c0 7.142-7.5 11.25-7.5 11.25S4.5 17.642 4.5 10.5a7.5 7.5 0 1115 0z" />
                        </svg>

                    </span>
                    <span>
                        Ver en Mapa
                    </span>
                </a>
            </div>
        </div>
    </div>
</template>

<style scoped>

</style>