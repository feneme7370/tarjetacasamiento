<script setup>
    const props = defineProps({
        hora: {type: String, required: true},
        titulo: {type: String, required: true},
        descripcion: {type: String, required: true},
    })
</script>

<template>
    <div class="flex items-center mb-8">
        <div class="bg-green-600 text-white rounded-full p-3">
            <span class="text-base mx-auto">{{ hora }}</span>
        </div>
        <div class="ml-4">
            <h2 class="text-sm font-bold">{{ titulo }}</h2>
            <p>{{ descripcion }}</p>
        </div>
    </div>
</template>

<style scoped>

</style>