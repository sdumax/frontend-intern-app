<template>
	<!-- image component -->
	<div class="image-container">
		<img src="../../src/assets/girl.png" alt="girl's image" />
	</div>
</template>

<script>
export default {
	name: "image-container",
};
</script>

<style scoped>
img {
	width: 20rem;
	height: auto;
	margin-top: 7.4rem;
}
.image-container {
	display: flex;
	/* margin-left: auto;
	margin-right: auto; */
	margin: auto;
	/* justify-content: center; */
	align-items: center;
	width: 22rem;
	height: 26rem;
	background: rgb(200, 41, 99);
	background: linear-gradient(
		156deg,
		rgba(200, 41, 99, 1) 57%,
		rgba(174, 24, 79, 1) 69%,
		rgba(171, 22, 77, 1) 100%
	);
	-webkit-box-shadow: 0px 0px 18px 9px rgba(0, 0, 0, 0.36);
	box-shadow: 0px 0px 18px 9px rgba(0, 0, 0, 0.36);
}
</style>
