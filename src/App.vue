<script setup>
import { ref, reactive, onMounted, watch } from 'vue';
import Cbu from './components/Cbu.vue';
import Portada from './components/Portada.vue';
import TarjetaEvento from './components/TarjetaEvento.vue';
import ItemItinerario from './components/ItemItinerario.vue';
import Frase1 from './components/Frase1.vue';
</script>

<template>

	<!-- portada -->
	<!-- <Portada /> -->
	<!-- <Frase1 /> -->

	<!-- siento que... -->
	<!-- <div class=" borde-primario bg-cover" style="background-image: url('/images/eucaliptus-6.jpg')">
		<div class="bg-opacity-50 bg-green-50 h-80 flex items-center justify-center">
			<div class="container mx-auto text-center cursiva">
				<h1 class="text-5xl font-bold mb-4">Yo si creo</h1>
				<p class="text-3xl mb-2 mt-5 font-bold">En un amor para toda la vida que sobreviva el tiempo, los obstaculos, los cambios y la vejez.</p>
			</div>
		</div>
	</div> -->
	<div class="mb-3">
		<img class="object-cover  mx-auto w-full " src="/public/images/nosotros13.png" alt="">
	</div>
	<div class="mb-1">
		<img class="rounded-2xl" src="/public/images/frase4.png" alt="">
	</div>

	<!-- Civil y Celebracion -->
	<div class="">
	<!-- <div class="bg-cover bg-center" style="background-image: url('/images/eucaliptus-5.jpg')"> -->
		<div class="bg-opacity-50 bg-green-50 h-min flex items-center justify-center">
			<div class="container mx-auto">

				<TarjetaEvento 
					:nombre="'Civil'"
					:fecha="'Fecha: 12 de Enero, 2024'"
					:lugar="'Lugar: Alsina 356, Pehuajo'"
					:imagen="'/images/nosotros6.jpeg'"
					:mapa="'https://www.google.com/maps/place/Registro+Civil/@-35.8111359,-61.9017263,16z/data=!4m10!1m2!2m1!1sregistro+civil+pehuajo+!3m6!1s0x95c0f82d5b461f57:0x4af780ced0f990a4!8m2!3d-35.8100811!4d-61.8987523!15sChZyZWdpc3RybyBjaXZpbCBwZWh1YWpvkgEPcmVnaXN0cnlfb2ZmaWNl4AEA!16s%2Fg%2F11dxl9y74q?hl=es&entry=ttu'"
				/>
				<TarjetaEvento 
					:nombre="'Celebracion'"
					:fecha="'Fecha: 13 de Enero, 2024'"
					:lugar="'Lugar: Ruta 5, Km 367, Pehuajo'"
					:imagen="'/images/nosotros12.jpeg'"
					:mapa="'https://www.google.com/maps/place/Arenales+356,+Carlos+Casares,+Provincia+de+Buenos+Aires/@-35.6197884,-61.3618965,17z/data=!3m1!4b1!4m5!3m4!1s0x95c0823ae11e9dd1:0x1c3caf321fdbb6b2!8m2!3d-35.6197928!4d-61.3593216?hl=es&entry=ttu'"
				/>

			</div>
		</div>
	</div>

	<!-- itinerario -->
	<div class="bg-white letra-primaria">
		<div class="container mx-auto py-8">
			<h1 class="text-5xl font-bold mb-6 text-center cursiva">Itinerario del Evento</h1>

			<div class="relative">

				<ItemItinerario
					:hora="'20:00'"
					:titulo="'Invitados'"
					:descripcion="'Llegada de los invitados'"
				/>
				<ItemItinerario
					:hora="'20:30'"
					:titulo="'Ceremonia'"
					:descripcion="'Llegada de la novia'"
				/>
				<ItemItinerario
					:hora="'21:00'"
					:titulo="'Recepcion'"
					:descripcion="'A degustar la entrada'"
				/>
				<ItemItinerario
					:hora="'22:30'"
					:titulo="'Cena'"
					:descripcion="'Mmmm... que rico'"
				/>
				<ItemItinerario
					:hora="'02:00'"
					:titulo="'Mesa Dulce'"
					:descripcion="'ñami ñani ;)'"
				/>
				<ItemItinerario
					:hora="'03:30'"
					:titulo="'Carioca'"
					:descripcion="'Pe pe pe pe'"
				/>
			</div>
		</div>
	</div>

	<div class="">
		<img class="rounded-2xl" src="/public/images/frase2.png" alt="">
	</div>

	<!-- galeria -->
	<div class="">
	<!-- <div class="bg-white"> -->
		<div class="container mx-auto py-8">
			<h1 class="text-5xl font-bold mb-6 text-center cursiva">Galería de Fotos</h1>

			<div class="grid grid-cols-1 md:grid-cols-4 gap-4">
				<div class="relative group cursor-pointer">
					<img src="/images/nosotros7.jpeg" alt="Foto 1" class="w-full h-96 object-cover rounded-lg transition duration-300 transform group-hover:scale-105">
					<div class="absolute inset-0 flex items-center justify-center opacity-0 group-hover:opacity-100 transition duration-300">
						<span class="text-white text-xl font-bold">Queremos</span>
					</div>
				</div>
				<div class="relative group cursor-pointer">
					<img src="/images/nosotros2.jpeg" alt="Foto 2" class="w-full h-96 object-cover rounded-lg transition duration-300 transform group-hover:scale-105">
					<div class="absolute inset-0 flex items-center justify-center opacity-0 group-hover:opacity-100 transition duration-300">
						<span class="text-white text-xl font-bold">Que</span>
					</div>
				</div>
				<div class="relative group cursor-pointer">
					<img src="/images/nosotros8.jpeg" alt="Foto 3" class="w-full h-96 object-cover rounded-lg transition duration-300 transform group-hover:scale-105">
					<div class="absolute inset-0 flex items-center justify-center opacity-0 group-hover:opacity-100 transition duration-300">
						<span class="text-white text-xl font-bold">Lo</span>
					</div>
				</div>
				<div class="relative group cursor-pointer">
					<img src="/images/nosotros4.jpeg" alt="Foto 4" class="w-full h-96 object-cover rounded-lg transition duration-300 transform group-hover:scale-105">
					<div class="absolute inset-0 flex items-center justify-center opacity-0 group-hover:opacity-100 transition duration-300">
						<span class="text-white text-xl font-bold">Disfrutes</span>
					</div>
				</div>
			</div>
		</div>
	</div>

	<!-- confirmar asistencia -->
	<div class="my-5">
	<!-- <div class="border-t-2 border-b-2 border-emerald-900"> -->

		<!-- <img src="/images/eucaliptus-4.jpg" alt=""> -->
		
		<div class="">
		<!-- <div class="bg-white"> -->
			<div class="container mx-auto py-8">
				<h1 class="text-4xl font-bold mb-10 text-center cursiva flex items-center justify-center gap-3">
					<span>
						<svg xmlns="http://www.w3.org/2000/svg" height="32" width="32" viewBox="0 0 448 512"><!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2023 Fonticons, Inc.--><path d="M380.9 97.1C339 55.1 283.2 32 223.9 32c-122.4 0-222 99.6-222 222 0 39.1 10.2 77.3 29.6 111L0 480l117.7-30.9c32.4 17.7 68.9 27 106.1 27h.1c122.3 0 224.1-99.6 224.1-222 0-59.3-25.2-115-67.1-157zm-157 341.6c-33.2 0-65.7-8.9-94-25.7l-6.7-4-69.8 18.3L72 359.2l-4.4-7c-18.5-29.4-28.2-63.3-28.2-98.2 0-101.7 82.8-184.5 184.6-184.5 49.3 0 95.6 19.2 130.4 54.1 34.8 34.9 56.2 81.2 56.1 130.5 0 101.8-84.9 184.6-186.6 184.6zm101.2-138.2c-5.5-2.8-32.8-16.2-37.9-18-5.1-1.9-8.8-2.8-12.5 2.8-3.7 5.6-14.3 18-17.6 21.8-3.2 3.7-6.5 4.2-12 1.4-32.6-16.3-54-29.1-75.5-66-5.7-9.8 5.7-9.1 16.3-30.3 1.8-3.7 .9-6.9-.5-9.7-1.4-2.8-12.5-30.1-17.1-41.2-4.5-10.8-9.1-9.3-12.5-9.5-3.2-.2-6.9-.2-10.6-.2-3.7 0-9.7 1.4-14.8 6.9-5.1 5.6-19.4 19-19.4 46.3 0 27.3 19.9 53.7 22.6 57.4 2.8 3.7 39.1 59.7 94.8 83.8 35.2 15.2 49 16.5 66.6 13.9 10.7-1.6 32.8-13.4 37.4-26.4 4.6-13 4.6-24.1 3.2-26.4-1.3-2.5-5-3.9-10.5-6.6z"/></svg>	
					</span>
					<span>Confirmanos tu asistencia</span>
				</h1>
				
				<div class=" flex items-center justify-center gap-2 montserrat">
					<a href="https://api.whatsapp.com/send/?phone=5492396513953&text=Confirmo asistencia a la Boda de Fede y Cinti" class="fondo-primario hover:fondo-primario-dark text-white font-light text-xl py-3 px-5 rounded focus:outline-none focus:shadow-outline text-center">
						Fede
					</a>
					<span>
						
					</span>
					<a href="https://api.whatsapp.com/send/?phone=5492396627259&text=Confirmo asistencia a la Boda de Fede y Cinti" class="fondo-primario hover:fondo-primario-dark text-white font-light text-xl py-3 px-5 rounded focus:outline-none focus:shadow-outline text-center">
						Cinti
					</a>
				</div>
			</div>
		</div>
		<!-- <img src="/images/eucaliptus-4.jpg" class="rotate-180" alt=""> -->
	</div>

	<!-- pedir tema -->
	<div class="fondo-primario">
		<div class="container mx-auto py-8">
			<h1 class="text-white text-5xl mb-6 text-center cursiva">Pedile un tema al DJ</h1>
			
				
				<div class=" flex items-center justify-center gap-4">
					<a href="https://api.whatsapp.com/send/?phone=5492396627259&text=Quiero bailar " class="fondo-primario hover:fondo-primario-dark text-white font-bold text-2xl py-3 px-3 rounded-3xl focus:outline-none focus:shadow-outline text-center border border-white flex items-center justify-center gap-4">
						<span class="text-white">
							<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
							<path stroke-linecap="round" stroke-linejoin="round" d="M9 9l10.5-3m0 6.553v3.75a2.25 2.25 0 01-1.632 2.163l-1.32.377a1.803 1.803 0 11-.99-3.467l2.31-.66a2.25 2.25 0 001.632-2.163zm0 0V2.25L9 5.25v10.303m0 0v3.75a2.25 2.25 0 01-1.632 2.163l-1.32.377a1.803 1.803 0 01-.99-3.467l2.31-.66A2.25 2.25 0 009 15.553z" />
							</svg>
						</span>
						<span class="cursiva text-3xl">Quiero bailar...</span>
						<span class="text-white">
							<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
							<path stroke-linecap="round" stroke-linejoin="round" d="M9 9l10.5-3m0 6.553v3.75a2.25 2.25 0 01-1.632 2.163l-1.32.377a1.803 1.803 0 11-.99-3.467l2.31-.66a2.25 2.25 0 001.632-2.163zm0 0V2.25L9 5.25v10.303m0 0v3.75a2.25 2.25 0 01-1.632 2.163l-1.32.377a1.803 1.803 0 01-.99-3.467l2.31-.66A2.25 2.25 0 009 15.553z" />
							</svg>
						</span>
					</a>
			</div>
		</div>
	</div>

	<!-- pedir bebida -->
	<div class="bg-cover bg-center border-t-2 borde-primario" style="background-image: url('/images/eucaliptus-2.jpg')">
		<div class="bg-opacity-20  h-60 flex items-center justify-center">
			<div class="container mx-auto text-center montserrat letra-primaria">
				<p class="text-lg my-1 px-5">Estamos organizando una fiesta al aire libre y esperamos que traigas tu propia bebida, para que podamos mantenernos hidratados y felices.</p>
				<span class=" flex items-center justify-center gap-1 letra-primaria">
					<svg xmlns="http://www.w3.org/2000/svg" height="32" width="32" viewBox="0 0 512 512"><!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2023 Fonticons, Inc.--><path fill="#305f64" d="M32 64c0-17.7 14.3-32 32-32H352c17.7 0 32 14.3 32 32V96h51.2c42.4 0 76.8 34.4 76.8 76.8V274.9c0 30.4-17.9 57.9-45.6 70.2L384 381.7V416c0 35.3-28.7 64-64 64H96c-35.3 0-64-28.7-64-64V64zM384 311.6l56.4-25.1c4.6-2.1 7.6-6.6 7.6-11.7V172.8c0-7.1-5.7-12.8-12.8-12.8H384V311.6zM160 144c0-8.8-7.2-16-16-16s-16 7.2-16 16V368c0 8.8 7.2 16 16 16s16-7.2 16-16V144zm64 0c0-8.8-7.2-16-16-16s-16 7.2-16 16V368c0 8.8 7.2 16 16 16s16-7.2 16-16V144zm64 0c0-8.8-7.2-16-16-16s-16 7.2-16 16V368c0 8.8 7.2 16 16 16s16-7.2 16-16V144z"/></svg>
					<svg xmlns="http://www.w3.org/2000/svg" height="32" width="32" viewBox="0 0 512 512"><!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2023 Fonticons, Inc.--><path fill="#305f64" d="M32 64c0-17.7 14.3-32 32-32H352c17.7 0 32 14.3 32 32V96h51.2c42.4 0 76.8 34.4 76.8 76.8V274.9c0 30.4-17.9 57.9-45.6 70.2L384 381.7V416c0 35.3-28.7 64-64 64H96c-35.3 0-64-28.7-64-64V64zM384 311.6l56.4-25.1c4.6-2.1 7.6-6.6 7.6-11.7V172.8c0-7.1-5.7-12.8-12.8-12.8H384V311.6zM160 144c0-8.8-7.2-16-16-16s-16 7.2-16 16V368c0 8.8 7.2 16 16 16s16-7.2 16-16V144zm64 0c0-8.8-7.2-16-16-16s-16 7.2-16 16V368c0 8.8 7.2 16 16 16s16-7.2 16-16V144zm64 0c0-8.8-7.2-16-16-16s-16 7.2-16 16V368c0 8.8 7.2 16 16 16s16-7.2 16-16V144z"/></svg>
					<svg xmlns="http://www.w3.org/2000/svg" height="32" width="32" viewBox="0 0 512 512"><!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2023 Fonticons, Inc.--><path fill="#305f64" d="M32 64c0-17.7 14.3-32 32-32H352c17.7 0 32 14.3 32 32V96h51.2c42.4 0 76.8 34.4 76.8 76.8V274.9c0 30.4-17.9 57.9-45.6 70.2L384 381.7V416c0 35.3-28.7 64-64 64H96c-35.3 0-64-28.7-64-64V64zM384 311.6l56.4-25.1c4.6-2.1 7.6-6.6 7.6-11.7V172.8c0-7.1-5.7-12.8-12.8-12.8H384V311.6zM160 144c0-8.8-7.2-16-16-16s-16 7.2-16 16V368c0 8.8 7.2 16 16 16s16-7.2 16-16V144zm64 0c0-8.8-7.2-16-16-16s-16 7.2-16 16V368c0 8.8 7.2 16 16 16s16-7.2 16-16V144zm64 0c0-8.8-7.2-16-16-16s-16 7.2-16 16V368c0 8.8 7.2 16 16 16s16-7.2 16-16V144z"/></svg>
				</span>
			</div>
		</div>
	</div>
	<div class="h-10 bg-white">

	</div>

	<!-- cbu -->

	<Cbu />

	<!-- <img src="/images/eucaliptus-4.jpg" class="rotate-180" alt=""> -->


</template>

<style scoped>

</style>