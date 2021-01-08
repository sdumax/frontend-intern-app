<template>
	<div id="app">
		<h2 class="h2">{{ jsonData.name }}</h2>
		<image-container></image-container>
		<Social :socialData="jsonData.social_media" />
		<page-nav></page-nav>
	</div>
</template>

<script>
import ImageContainer from "./components/ImageContainer.vue";
import PageNav from "./components/PageNav.vue";
import Social from "./components/Social.vue";

export default {
	name: "App",
	components: {
		Social,
		ImageContainer,
		PageNav,
	},
	created() {
		// fetch data
		fetch("https://hirng-x2021.glitch.me/api").then(async (response) => {
			const data = await response.json();

			// error check
			if (!response.ok) {
				const error = (data && data.message) || response.status;
				return Promise.reject(error);
			}
			this.jsonData = data;
		});
	},
	data() {
		return {
			jsonData: {},
		};
	},
};
</script>

<style>
body {
	font-family: Verdana, Geneva, Tahoma, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	font-weight: 500;
	color: rgb(245, 245, 245);
	margin-top: 20px;
	background: rgb(189, 15, 77);
	background: linear-gradient(
		90deg,
		rgba(189, 15, 77, 1) 50%,
		rgba(203, 41, 100, 1) 50%
	);
}
ul {
	list-style-type: none;
	padding: 0;
}
li {
	display: inline-block;
	margin: 0 10px;
}
a {
	color: inherit;
}
.h2 {
	margin: 1.5rem;
}
</style>
