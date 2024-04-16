<script>
	import './style.css'

	export default {
		data() {
			return {
				title: "Eriksson",
				username: "@erikssonnn",
				description: "~Aspiring game developer~",
			}
		},

		methods: {
			openLink(url){
				window.open(url, "_blank");
			}
		},

		mounted() {
			// do nothing for now
		}
	}
</script>

<template>
	<div class="page">
	  	<div class="navbar"></div>

		<div class="wrapper">
			<span class="picture-wrapper">
				<img class="picture" src="./assets/img_second.jpg" />
			</span>

			<h1>{{title}}</h1>
			<h3>{{username}}</h3>
			<h3>{{description}}</h3>
			
			<span class="link-wrapper">
				<img class="link-img" @click="openLink('https://www.linkedin.com/in/carl-eriksson-43891222b/')" src="./assets/linkedin.png">
				<img class="link-img" @click="openLink('https://erikssonnn.itch.io/')" src="./assets/itch.png">
				<img class="link-img" @click="openLink('https://carl_erikssonn.artstation.com/')" src="./assets/artstation.png">
				<img class="link-img" @click="openLink('https://github.com/erikssonnn')" src="./assets/github.png">
				<!-- <img class="link-img" @click="openLink('https://twitter.com/erikssonnn_')" src="./assets/twitter.png"> -->
			</span>
		</div>
	</div>
</template>

<style>

</style>