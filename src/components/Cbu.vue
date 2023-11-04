<script setup>

</script>

<template>
	<div class="bg-green-100">
		<div class="container mx-auto py-8">
			<h1 class="text-3xl font-bold mb-6 text-center">Si queres colaborar</h1>

			<div class="bg-white p-6 rounded-lg shadow-md">
				<div class="accordion">
					<input type="checkbox" class="accordion-checkbox" id="panel1">
					<label class="accordion-label cursor-pointer" for="panel1">
						<h2 class="text-xl font-semibold">Haz una Donación</h2>
						<div class="accordion-icon">&#x25BC;</div>
					</label>
					<div class="accordion-content">
						<p class="text-lg font-semibold">1234 5678 9012 3456</p>
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
				padding: 1rem;
				border-bottom: 1px solid #ccc;
			}

			.accordion-icon {
				font-size: 1.5rem;
			}

			.accordion-content {
				display: none;
				padding: 1rem;
			}

			.accordion-checkbox:checked+.accordion-label .accordion-icon {
				transform: rotate(180deg);
			}

			.accordion-checkbox:checked+.accordion-label+.accordion-content {
				display: block;
			}
</style>