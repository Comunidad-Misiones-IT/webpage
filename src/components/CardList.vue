<template>
	<div class="links container-fluid">
		<Card 
		v-for="(card, index) in cards"
		v-bind="card"
		:key="index" />
	</div>
</template>

<script>
	import Card from './Card';

	export default {
		components: {
			Card
		},
		data () {
			return {
				cards: [
					{
						nombre: "Discord",
						img_src: "/img/discord.png",
						link_src: "https://discord.com/invite/6Tkv8pn"
					},
					{
						nombre: "Instagram",
						img_src: "/img/instagram.png",
						link_src: "https://www.instagram.com/comunidadmit/"
					},
					{
						nombre: "Twitter",
						img_src: "/img/twitter.png",
						link_src: "https://twitter.com/ComunidadMIT"
					},
					{
						nombre: "LinkedIn",
						img_src: "/img/linkedin.png",
						link_src: "https://www.linkedin.com/company/comunidad-mit/"
					},
					{
						nombre: "Github",
						img_src: "/img/github.png",
						link_src: "https://github.com/Comunidad-Misiones-IT"
					},
					{
						nombre: "Spotify",
						img_src: "/img/spotify.png",
						link_src: "https://open.spotify.com/user/5bgl2oo5nvp4is4ihv6u4umet"
					},
					{
						nombre: "Twitch",
						img_src: "/img/twitch.png",
						link_src: "https://www.twitch.tv/comunidadmit"
					},
					{
						nombre: "Email",
						img_src: "/img/email.png",
						link_src: "mailto:hola@comit.ar"
					},
					{
						nombre: "WEBINAR: Programar desde Misiones",
						img_src: "/img/youtube.png",
						link_src: "https://www.youtube.com/watch?v=tabBLNTPInQ"
					}
				]
			}
		}
	}
</script>

<style>
	.links {
		padding: 0.2em 1.6em;
	}
</style>