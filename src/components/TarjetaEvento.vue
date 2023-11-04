<script setup>
    const props = defineProps({
        nombre: {type: String, required: true},
        fecha: {type: String, required: true},
        lugar: {type: String, required: true},
    })
</script>

<template>
    <div class="max-w-md mx-auto bg-white rounded-md shadow-md overflow-hidden mb-4">
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTrgIPYsmANFcWiN7q8THaXm6IfzMXLEsdLJQ&usqp=CAU" alt="Evento 1" class="w-full h-32 object-cover">
        <div class="p-4">
            <h2 class="text-2xl font-bold mb-2">{{ nombre }}</h2>
            <p class="text-sm mb-2">Fecha: 12 de Enero, 2024</p>
            <p class="text-sm mb-2">Lugar: Alsina 356, Pehuajo</p>
        </div>
    </div>
</template>

<style scoped>

</style>