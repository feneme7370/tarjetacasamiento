<script setup>

</script>

<template>
	<div class="bg-green-100">
		<div class="mx-auto pt-8">
			<h1 class="text-4xl font-bold mb-6 text-center cursiva">Nuestro Regalo</h1>
			<p class="container text-2xl text-center cursiva">Es tu presencia pero si ademas quieres colaborar con nuestro proyecto de vida</p>

			<div class="bg-white p-1 mt-4">
				<div class="accordion">
					<input type="checkbox" class="accordion-checkbox" id="panel1">
					<label class="accordion-label cursor-pointer" for="panel1">
						<h2 class="text-xl pl-10">Ver CBU</h2>
						<div class="accordion-icon">&#x25BC;</div>
					</label>
					<div class="accordion-content">
						<p class="text-base text-center my-3">1234567890123456</p>
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