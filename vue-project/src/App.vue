<script>
	export default {
		data() {
			return {
				title: "Eriksson",
				username: "@erikssonnn",
				description: "~Aspiring game developer~",
				links: [
					{ url: "./assets/itch.png", name: 'Link 1' },
					{ url: "./assets/artstation.png", name: 'Link 2' },
					{ url: "./assets/twitter.png", name: 'Link 3' },
				],
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
			<img class="picture" src="./assets/img.jpg" />
			<h1>{{title}}</h1>
			<h3>{{username}}</h3>
			<h3>{{description}}</h3>
			<span class="link-wrapper">
				<img class="link-img" @click="openLink('https://www.linkedin.com/in/carl-eriksson-43891222b/')" src="./assets/linkedin.png">
				<img class="link-img" @click="openLink('https://erikssonnn.itch.io/')" src="./assets/itch.png">
				<img class="link-img" @click="openLink('https://carl_erikssonn.artstation.com/')" src="./assets/artstation.png">
				<img class="link-img" @click="openLink('https://github.com/erikssonnn')" src="./assets/github.png">
				<img class="link-img" @click="openLink('https://twitter.com/erikssonnn_')" src="./assets/twitter.png">
			</span>
		</div>
	</div>
</template>

<style >
	@font-face {
		font-family: 'CustomFont';
		src: url('./assets/font.ttf') format('truetype');
	}

	body{
		margin: 0px;
	}

	.page {
		overflow: hidden;
		display: flex;
		flex-direction: column;
		height: 100vh;
	}

	.navbar {
		width: 100%;
		height: 15%;
		background-color: #212121;
	}

	.wrapper {
		width: 100%;
		height: 100%;
		background-color: #292929;
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	.link-wrapper {
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
		width: 100%;
		height: 5vh;
		gap: 1vh;
		margin-top: 3vh;
		overflow: hidden;
	}

	/* pictures */
	.picture {
		margin: 2vh;
		height: 25vh;
		width: 25vh;
		border-radius: 50%;
		object-fit: cover;
		object-position: center;
		outline: 0.25vh solid whitesmoke;
	}

	.link-img{
		height: 4vh;
		width: 4vh;
		margin: 2vh;
		border-radius: 50%;
		object-fit: cover;
		object-position: center;
		outline: 0.4vh solid black;
		outline-offset: -0.25vh;
		transition: transform 0.2s ease;
	}

	.link-img:hover{
		transform: scale(1.2);
	}

	/* LABELS */
	label, h1, h2, h3 {
		font-family: 'CustomFont', sans-serif;
		margin-top: 0.5vh;
		margin-bottom: 0.5vh;
		color: whitesmoke;
	}
</style>
