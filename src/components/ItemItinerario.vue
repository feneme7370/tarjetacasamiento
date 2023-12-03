<script setup>
    const props = defineProps({
        hora: {type: String, required: true},
        titulo: {type: String, required: true},
        descripcion: {type: String, required: true},
    })
</script>

<template>
    <div class="flex items-center mb-8 montserrat">
        <div class="fondo-primario text-white rounded-full p-3">
            <span class="text-lg mx-auto">{{ hora }}</span>
        </div>
        <div class="ml-4">
            <h2 class=" text-xl font-bold">{{ titulo }}</h2>
            <p class=" text-base font-light">{{ descripcion }}</p>
        </div>
    </div>
</template>

<style scoped>

</style>