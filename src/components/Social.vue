<template>
	<div class="">
		<div class="social-container">
			<ul class="social-icon-group">
				<li v-for="icon in icons" :key="icon.name" class="social-icon">
					<a :href="icon.url + icon.link"> <i :class="icon.name"></i></a>
				</li>
			</ul>
		</div>
	</div>
</template>

<script>
export default {
	name: "Social",
	props: {
		socialData: Object,
	},

	data: function() {
		return {
			icons: [
				{
					name: "fab fa-instagram",
					url: "https://instagram.com/",
					link: this.socialData.instagram,
				},
				{
					name: "fab fa-twitter-square",
					url: "https://twiiter.com/",
					link: this.socialData.twitter,
				},
				{
					name: "fab fa-snapchat-square",
					url: "https://snapchat.com/",
					link: this.socialData.snapchat,
				},
				{
					name: "fas fa-envelope-square",
					url: "https://gmail.com/",
					link: this.socialData.email,
				},
			],
		};
	},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
	margin: 40px 0 0;
}

.social-container {
	position: absolute;
	right: 0;
	top: 50%;
	transform: translateY(-50%);
}
.social-icon-group {
	/* position: absolute; */
	display: flex;
	justify-content: center;
	align-items: center;
	flex-direction: column;
	padding: 0.5rem;
}
.social-icon {
	margin: 0.4rem;
	font-size: 24px;
}
</style>
