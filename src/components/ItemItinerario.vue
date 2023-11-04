<script setup>
    const props = defineProps({
        hora: {type: String, required: true},
        titulo: {type: String, required: true},
        descripcion: {type: String, required: true},
    })
</script>

<template>
    <div class="flex items-center mb-8">
        <div class="bg-emerald-700 text-white rounded-full p-3">
            <span class="text-lg mx-auto">{{ hora }}</span>
        </div>
        <div class="ml-4">
            <h2 class="text-lg font-bold">{{ titulo }}</h2>
            <p class="text-lg font-bold">{{ descripcion }}</p>
        </div>
    </div>
</template>

<style scoped>

</style>