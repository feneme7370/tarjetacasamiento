<script setup>
import { ref, reactive, onMounted, watch } from 'vue';
import Cbu from './components/Cbu.vue';
import Portada from './components/Portada.vue';
import TarjetaEvento from './components/TarjetaEvento.vue';
import ItemItinerario from './components/ItemItinerario.vue';

</script>

<template>

	<!-- portada -->
	<Portada />

	<!-- texto sentimos que... -->
	<div class="sm:mb-32 mb-10 border-t-2 border-b-2 border-emerald-900" style="background-image: url('/images/eucaliptus-2.jpg')">
		<div class="bg-opacity-50 bg-green-50 h-80 flex items-center justify-center">
			<div class="container mx-auto text-center cursiva">
				<h1 class="text-4xl font-bold mb-4">Sentimos que...</h1>
				<p class="text-2xl mb-2">Cuando te das cuenta de que quieres pasar el resto de tu vida con alguien, deseas que el resto de tu
					vida empiece lo antes posible.</p>
			</div>
		</div>
	</div>


	<!-- Civil y Celebracion -->
	<div class="bg-cover bg-center" style="background-image: url('/images/eucaliptus-5.jpg')">
		<div class="bg-opacity-50 bg-green-50 h-min flex items-center justify-center">
			<div class="container mx-auto">

				<TarjetaEvento 
					:nombre="'Civil'"
					:fecha="'Fecha: 12 de Enero, 2024'"
					:lugar="'Lugar: Alsina 356, Pehuajo'"
					:imagen="'/images/nosotros1.jpeg'"
					:mapa="'https://www.google.com/maps/place/Registro+Civil/@-35.8111359,-61.9017263,16z/data=!4m10!1m2!2m1!1sregistro+civil+pehuajo+!3m6!1s0x95c0f82d5b461f57:0x4af780ced0f990a4!8m2!3d-35.8100811!4d-61.8987523!15sChZyZWdpc3RybyBjaXZpbCBwZWh1YWpvkgEPcmVnaXN0cnlfb2ZmaWNl4AEA!16s%2Fg%2F11dxl9y74q?hl=es&entry=ttu'"
				/>
				<TarjetaEvento 
					:nombre="'Celebracion'"
					:fecha="'Fecha: 13 de Enero, 2024'"
					:lugar="'Lugar: Ruta 366, Pehuajo'"
					:imagen="'/images/nosotros2.jpeg'"
					:mapa="'https://www.google.com/maps/place/Arenales+356,+Carlos+Casares,+Provincia+de+Buenos+Aires/@-35.6197884,-61.3618965,17z/data=!3m1!4b1!4m5!3m4!1s0x95c0823ae11e9dd1:0x1c3caf321fdbb6b2!8m2!3d-35.6197928!4d-61.3593216?hl=es&entry=ttu'"
				/>

			</div>
		</div>
	</div>

	<!-- itinerario -->
	<div class="bg-white text-green-900">
		<div class="container mx-auto py-8">
			<h1 class="text-4xl font-bold mb-6 text-center cursiva">Itinerario del Evento</h1>

			<div class="relative">

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

	<!-- siento que... -->
	<div class="border-t-2 border-b-2 border-emerald-900" style="background-image: url('/images/eucaliptus-2.jpg')">
		<div class="bg-opacity-50 bg-green-50 h-80 flex items-center justify-center">
			<div class="container mx-auto text-center cursiva">
				<h1 class="text-4xl font-bold mb-4">Yo si creo</h1>
				<p class="text-2xl mb-2">En un amor para toda la vida que sobreviva el tiempo, los obstaculos, los cambios y la vejez.</p>
			</div>
		</div>
	</div>

	<!-- galeria -->
	<div class="bg-white">
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

	<!-- confirmar asistencia -->
	<div class="border-t-2 border-b-2 border-emerald-900">

		<img src="/images/eucaliptus-4.jpg" alt="">
		
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

	<!-- pedir tema -->
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

	<!-- pedir bebida -->
	<div class="bg-cover bg-center border-t-2 border-b-2 border-emerald-900" style="background-image: url('/images/eucaliptus-2.jpg')">
		<div class="bg-opacity-50 bg-green-50 h-60 flex items-center justify-center">
			<div class="container mx-auto text-center cursiva">
				<p class="text-3xl font-bold mb-2">Estamos organizando una fiesta al aire libre y esperamos que traigas tu propia bebida, para que podamos mantenernos hidratados y felices.</p>
			</div>
		</div>
	</div>

	<!-- cbu -->

	<Cbu />

	<img src="/images/eucaliptus-4.jpg" class="rotate-180" alt="">


</template>

<style scoped>

</style>