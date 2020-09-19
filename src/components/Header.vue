<template>
	<div>
		<div class="mb-2">
			<button type="button" class="btn" @click="cambiarModo">🌞|🌚</button>
		</div>

		<img src="/img/mit.png" class="avatar img" alt="avatar" />
		<h1>Misiones IT</h1>

		<div class="m-2 desc">
			<p>Somos una comunidad convencida de que Misiones tiene talento valioso para la industria IT, y lo queremos potenciar. Si queres saber que hay detrás de esta pagina, manijear juegos o compartir experiencias seguí a MIT en sus redes:</p>
		</div>
	</div>
</template>

<script>
	export default {
		methods: {
			cambiarModo() { 
				document.body.classList.toggle("oscuro"); 
			}
		}
	}
</script>

<style>
	.oscuro button {
		color: #f1eded;
	}

	button:hover {
		color: #f1eded;
	}

	button:focus {
		outline:0;
	}
</style>