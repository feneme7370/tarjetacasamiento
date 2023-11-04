<script setup>
import { ref, reactive, onMounted, watch } from 'vue';
import Cbu from './components/Cbu.vue';
import Portada from './components/Portada.vue';
import TarjetaEvento from './components/TarjetaEvento.vue';
import ItemItinerario from './components/ItemItinerario.vue';

</script>

<template>
	<!-- Imagen de fondo con opacidad -->
	<!-- <img src="https://c.wallhere.com/photos/71/03/ring_dress_engagement_couple_wedding-787371.jpg!d" alt="Imagen de fondo" class="absolute inset-0 w-full h-full object-cover opacity-50"> -->

	<!-- portada -->
	<Portada />

	<!-- texto sentimos que... -->

	<div class="sm:mb-32 mb-16" style="background-image: url('https://img.freepik.com/fotos-premium/marco-hojas-eucalipto-verde-tarjeta-ilustracion-acuarela-aislado-sobre-fondo-blanco-dibujado-mano_596988-187.jpg')">
		<div class="bg-opacity-50 bg-green-50 h-80 flex items-center justify-center">
			<div class="container mx-auto text-center">
				<h1 class="text-4xl font-bold mb-4">Sentimos que...</h1>
				<p class="text-sm mb-2">Cuando te das cuenta de que quieres pasar el resto de tu vida con alguien, deseas que el resto de tu
					vida empiece lo antes posible.</p>
			</div>
		</div>
	</div>

	<!-- Civil y Celebracion -->
	<div class="bg-cover bg-center sm:mb-32 mb-16" style="background-image: url('https://static.vecteezy.com/system/resources/previews/009/667/576/non_2x/seamless-watercolor-pattern-with-eucalyptus-leaves-on-a-white-background-vintage-pattern-with-green-tropical-eucalyptus-leaves-design-for-wallpaper-fabric-postcards-covers-vector.jpg')">
		<div class="bg-opacity-50 bg-green-50 h-screen flex items-center justify-center">
			<div class="container mx-auto">

				<TarjetaEvento 
					:nombre="'Civil'"
					:fecha="'Fecha: 12 de Enero, 2024'"
					:lugar="'Lugar: Alsina 356, Pehuajo'"
				/>
				<TarjetaEvento 
					:nombre="'Celebracion'"
					:fecha="'Fecha: 13 de Enero, 2024'"
					:lugar="'Lugar: Ruta 366, Pehuajo'"
				/>

			</div>
		</div>
	</div>

	<!-- itinerario -->
	<div class="bg-green-50 text-green-900">
		<div class="container mx-auto py-8">
			<h1 class="text-3xl font-bold mb-6 text-center">Itinerario del Evento</h1>

			<div class="relative">
				<!-- <div class="absolute h-full w-1 bg-green-600 left-1/2 transform -translate-x-1/2"></div> -->

				<ItemItinerario
					:hora="'20:30'"
					:titulo="'Registro y Recepción de Invitados'"
					:descripcion="'Lugar: Quinta'"
				/>
				<ItemItinerario
					:hora="'21:45'"
					:titulo="'Llegada de los novios'"
					:descripcion="'Comer entrada'"
				/>
				<ItemItinerario
					:hora="'22:30'"
					:titulo="'Comida'"
					:descripcion="'Sentarse en las mesas'"
				/>
				<ItemItinerario
					:hora="'23:30'"
					:titulo="'Primer Baile'"
					:descripcion="'A mover las cachas'"
				/>
				<ItemItinerario
					:hora="'01:30'"
					:titulo="'Mesa Dulce'"
					:descripcion="'Mmmm..'"
				/>
				<ItemItinerario
					:hora="'02:30'"
					:titulo="'Segundo baile'"
					:descripcion="'A seguir moviendo'"
				/>
			</div>
		</div>
	</div>

	<!-- galeria -->
	<div class="bg-green-100">
		<div class="container mx-auto py-8">
			<h1 class="text-3xl font-bold mb-6 text-center">Galería de Fotos</h1>

			<div class="grid grid-cols-1 md:grid-cols-4 gap-4">
				<div class="relative group cursor-pointer">
					<img src="https://media.ambito.com/p/39b277b2257086a12bb02ee0d5670dba/adjuntos/239/imagenes/040/617/0040617596/1200x675/smart/casamientojpg.jpg" alt="Foto 1" class="w-full h-48 object-cover rounded-lg transition duration-300 transform group-hover:scale-105">
					<div class="absolute inset-0 flex items-center justify-center opacity-0 group-hover:opacity-100 transition duration-300">
						<span class="text-white text-xl font-bold">Queremos</span>
					</div>
				</div>
				<div class="relative group cursor-pointer">
					<img src="https://media.ambito.com/p/39b277b2257086a12bb02ee0d5670dba/adjuntos/239/imagenes/040/617/0040617596/1200x675/smart/casamientojpg.jpg" alt="Foto 2" class="w-full h-48 object-cover rounded-lg transition duration-300 transform group-hover:scale-105">
					<div class="absolute inset-0 flex items-center justify-center opacity-0 group-hover:opacity-100 transition duration-300">
						<span class="text-white text-xl font-bold">Que</span>
					</div>
				</div>
				<div class="relative group cursor-pointer">
					<img src="https://media.ambito.com/p/39b277b2257086a12bb02ee0d5670dba/adjuntos/239/imagenes/040/617/0040617596/1200x675/smart/casamientojpg.jpg" alt="Foto 3" class="w-full h-48 object-cover rounded-lg transition duration-300 transform group-hover:scale-105">
					<div class="absolute inset-0 flex items-center justify-center opacity-0 group-hover:opacity-100 transition duration-300">
						<span class="text-white text-xl font-bold">Lo</span>
					</div>
				</div>
				<div class="relative group cursor-pointer">
					<img src="https://media.ambito.com/p/39b277b2257086a12bb02ee0d5670dba/adjuntos/239/imagenes/040/617/0040617596/1200x675/smart/casamientojpg.jpg" alt="Foto 4" class="w-full h-48 object-cover rounded-lg transition duration-300 transform group-hover:scale-105">
					<div class="absolute inset-0 flex items-center justify-center opacity-0 group-hover:opacity-100 transition duration-300">
						<span class="text-white text-xl font-bold">Disfrutes</span>
					</div>
				</div>
			</div>
		</div>
	</div>

	<!-- texto agradecimiento -->
	<div class="bg-green-100">
		<div class="container mx-auto py-8">
			<h1 class="text-3xl font-bold mb-6 text-center">Agradecimiento</h1>
			
			<div class="bg-white p-6 rounded-lg shadow-md italic">
				<p class="text-lg mb-4">Queremos expresar nuestro más sincero agradecimiento por tu participación en nuestro evento. Tu presencia y apoyo han hecho que este día sea realmente especial.</p>
				<p class="text-lg">Atentamente,<br>Fede y Cinti</p>
			</div>
		</div>
	</div>

	<!-- cbu -->

	<Cbu />

</template>

<style scoped>

</style>