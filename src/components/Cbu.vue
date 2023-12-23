<script setup>

</script>

<template>
	<div class="py-5 fondo-secundario">
		<div class="mx-auto">
			<h1 class="text-5xl font-bold mb-6 text-center cursiva flex items-center justify-center gap-3">
				<span>
					<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-8 h-8">
						<path stroke-linecap="round" stroke-linejoin="round" d="M21 11.25v8.25a1.5 1.5 0 01-1.5 1.5H5.25a1.5 1.5 0 01-1.5-1.5v-8.25M12 4.875A2.625 2.625 0 109.375 7.5H12m0-2.625V7.5m0-2.625A2.625 2.625 0 1114.625 7.5H12m0 0V21m-8.625-9.75h18c.621 0 1.125-.504 1.125-1.125v-1.5c0-.621-.504-1.125-1.125-1.125h-18c-.621 0-1.125.504-1.125 1.125v1.5c0 .621.504 1.125 1.125 1.125z" />
					</svg>
				</span>
				<span>
					Nuestro Regalo
				</span>
			</h1>
			<p class="container text-lg px-2 text-center montserrat"><span class="font-bold">Es tu presencia</span>, pero si ademas quieres colaborar con nuestro proyecto de vida</p>

			<div class="p-1 mt-4 px-5 montserrat">
				<div class="accordion border-2 borde-primario rounded-3xl ">
					<input type="checkbox" class="accordion-checkbox" id="panel1">
					<label class="accordion-label cursor-pointer px-2" for="panel1">
						<h2 class="text-lg pl-5">VER CBU</h2>
						<div class="accordion-icon">&#x25BC;</div>
					</label>
					<div class="accordion-content">
						<p class="text-base font-bold text-center my-3">0140308203673852562164</p>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<style scoped>
			.accordion-checkbox {
				display: none;
			}

			.accordion-label {
				display: flex;
				justify-content: space-between;
				align-items: center;
				cursor: pointer;
				/* padding: 1rem; */
				/* border-bottom: 1px solid #ccc; */
			}

			.accordion-icon {
				font-size: 1.5rem;
			}

			.accordion-content {
				display: none;
				/* padding: 1rem; */
			}

			.accordion-checkbox:checked+.accordion-label .accordion-icon {
				transform: rotate(180deg);
			}

			.accordion-checkbox:checked+.accordion-label+.accordion-content {
				display: block;
			}
</style>