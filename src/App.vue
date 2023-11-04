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

	<div class="sm:mb-32 mb-10 border-t-2 border-b-2 border-emerald-900" style="background-image: url('/images/eucaliptus-2.jpg')">
		<div class="bg-opacity-50 bg-green-50 h-80 flex items-center justify-center">
			<div class="container mx-auto text-center cursiva">
				<h1 class="text-4xl font-bold mb-4">Sentimos que...</h1>
				<p class="text-lg mb-2">Cuando te das cuenta de que quieres pasar el resto de tu vida con alguien, deseas que el resto de tu
					vida empiece lo antes posible.</p>
			</div>
		</div>
	</div>


	<!-- Civil y Celebracion -->
	<div class="bg-cover bg-center sm:mb-32 mb-16" style="background-image: url('/images/eucaliptus-5.jpg')">
		<div class="bg-opacity-50 bg-green-50 h-min flex items-center justify-center">
			<div class="container mx-auto">

				<TarjetaEvento 
					:nombre="'Civil'"
					:fecha="'Fecha: 12 de Enero, 2024'"
					:lugar="'Lugar: Alsina 356, Pehuajo'"
					:imagen="'/images/nosotros1.jpeg'"
				/>
				<TarjetaEvento 
					:nombre="'Celebracion'"
					:fecha="'Fecha: 13 de Enero, 2024'"
					:lugar="'Lugar: Ruta 366, Pehuajo'"
					:imagen="'/images/nosotros2.jpeg'"
				/>

			</div>
		</div>
	</div>

	<!-- itinerario -->
	<div class="bg-green-50 text-green-900">
		<div class="container mx-auto py-8">
			<h1 class="text-4xl font-bold mb-6 text-center cursiva">Itinerario del Evento</h1>

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
			<h1 class="text-4xl font-bold mb-6 text-center cursiva">Galería de Fotos</h1>

			<div class="grid grid-cols-1 md:grid-cols-4 gap-4">
				<div class="relative group cursor-pointer">
					<img src="/images/nosotros1.jpeg" alt="Foto 1" class="w-full h-80 object-cover rounded-lg transition duration-300 transform group-hover:scale-105">
					<div class="absolute inset-0 flex items-center justify-center opacity-0 group-hover:opacity-100 transition duration-300">
						<span class="text-white text-xl font-bold">Queremos</span>
					</div>
				</div>
				<div class="relative group cursor-pointer">
					<img src="/images/nosotros2.jpeg" alt="Foto 2" class="w-full h-80 object-cover rounded-lg transition duration-300 transform group-hover:scale-105">
					<div class="absolute inset-0 flex items-center justify-center opacity-0 group-hover:opacity-100 transition duration-300">
						<span class="text-white text-xl font-bold">Que</span>
					</div>
				</div>
				<div class="relative group cursor-pointer">
					<img src="/images/nosotros3.jpeg" alt="Foto 3" class="w-full h-80 object-cover rounded-lg transition duration-300 transform group-hover:scale-105">
					<div class="absolute inset-0 flex items-center justify-center opacity-0 group-hover:opacity-100 transition duration-300">
						<span class="text-white text-xl font-bold">Lo</span>
					</div>
				</div>
				<div class="relative group cursor-pointer">
					<img src="/images/nosotros4.jpeg" alt="Foto 4" class="w-full h-80 object-cover rounded-lg transition duration-300 transform group-hover:scale-105">
					<div class="absolute inset-0 flex items-center justify-center opacity-0 group-hover:opacity-100 transition duration-300">
						<span class="text-white text-xl font-bold">Disfrutes</span>
					</div>
				</div>
			</div>
		</div>
	</div>

	<div class="border-t-2 border-b-2 border-emerald-900">

		<img src="/images/eucaliptus-4.jpg" alt="">
		<!-- confirmar asistencia -->
		<div class="bg-white">
			<div class="container mx-auto py-8">
				<h1 class="text-4xl font-bold mb-10 text-center cursiva">Confirmanos tu asistencia</h1>
				
				<div class=" flex items-center justify-center gap-2">
					<a href="https://api.whatsapp.com/send/?phone=5492396513953&text=Confirmo asistencia a la Boda de Fede y Cinti" class="bg-emerald-700 hover:bg-emerald-800 text-white font-bold text-xl py-3 px-5 rounded focus:outline-none focus:shadow-outline text-center">
						Fede
					</a>
					<a href="https://api.whatsapp.com/send/?phone=5492396627259&text=Confirmo asistencia a la Boda de Fede y Cinti" class="bg-emerald-700 hover:bg-emerald-800 text-white font-bold text-xl py-3 px-5 rounded focus:outline-none focus:shadow-outline text-center">
						Cinti
					</a>
				</div>
			</div>
		</div>
		<img src="/images/eucaliptus-4.jpg" class="rotate-180" alt="">
	</div>
	<!-- texto agradecimiento -->
	<div class="bg-green-100">
		<div class="container mx-auto py-8">
			<h1 class="text-4xl font-bold mb-6 text-center cursiva">Pedile un tema al DJ</h1>
			
			<div class="bg-white p-6 rounded-lg shadow-md italic">
				
				<div class=" flex items-center justify-center gap-2">
					<a href="https://api.whatsapp.com/send/?phone=5492396627259&text=Quiero bailar " class="bg-emerald-700 hover:bg-emerald-800 text-white font-bold text-xl py-3 px-5 rounded focus:outline-none focus:shadow-outline text-center">
						Quiero bailer...
					</a>
				</div>
			</div>
		</div>
	</div>

	<!-- cbu -->

	<Cbu />

	<img src="/images/eucaliptus-4.jpg" class="rotate-180" alt="">


</template>

<style scoped>

</style>