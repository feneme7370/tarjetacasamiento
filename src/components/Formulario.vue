<script setup>
    const props = defineProps({
        alerta : {type: Object, deep:true},
        usuario : {type: Object, deep:true}
    })

    const emits = defineEmits(['guardar'])
</script>

<template>
    <form class="form" @submit.prevent="$emit('guardar')">
        <div :class="alerta.tipo === 'error' ? 'bg-red-500' : 'bg-green-500'" v-if="alerta.tipo">
          {{ alerta.mensaje }}
        </div>
        <div class="campo">
          <label for="id">Id</label>
          <input id="id" type="text" v-model="usuario.id">
        </div>
        <div class="campo">
          <label for="nombre">Nombre</label>
          <input id="nombre" type="text" v-model="usuario.nombre">
        </div>
        <div class="campo">
          <label for="fecha">Fecha</label>
          <input id="fecha" type="date" v-model="usuario.fecha">
        </div>
  
        <input type="submit" :value="usuario.id ? 'editar' : 'registrar'">
      </form>
</template>

<style scoped>

</style>