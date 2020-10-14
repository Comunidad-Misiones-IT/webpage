<template>
	<div>
		<div class="mb-2">
			<button type="button" class="btn" @click="cambiarModo">🌞|🌚</button>
		</div>

		<img src="/img/mit.png" class="avatar img" alt="avatar" />
		<h1>Misiones IT</h1>

		<div class="m-2 desc">
			<p>Somos una comunidad convencida de que Misiones tiene talento valioso para la industria IT, y lo queremos potenciar. Si querés saber qué hay detrás de esta página, manijear juegos o compartir experiencias, seguí a MIT en sus redes:</p>
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
	.avatar {
		width: 7em;
		margin-bottom: 1em;
		margin-top: 0.2em;
	}

	.oscuro h1 { 
		color: #f1eded;
	}

	.oscuro button {
		color: #f1eded;
	}

	.oscuro .desc {
		color: white;
	}

	button:hover {
		color: #f1eded;
	}

	button:focus {
		outline:0;
	}
	
	h1, h2 {
		font-weight: normal;
		font-size: 2.5rem;
		text-transform: uppercase;
		letter-spacing: 0.1em;
	}
</style>
