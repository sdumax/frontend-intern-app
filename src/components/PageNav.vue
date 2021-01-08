<template>
	<div>
		<ul class="page-nav">
			<li class="nav-link">home</li>
			<li class="nav-link">about</li>
			<li class="nav-link image">
				<img src="../assets/girl-circular.png" alt="" />
			</li>
			<li class="nav-link">gallery</li>
			<li class="nav-link">contact</li>
		</ul>
	</div>
</template>

<script>
export default {
	name: "PageNav",
};
</script>

<style scoped>
.page-nav {
	text-transform: uppercase;
	display: flex;
	justify-content: center;
	align-items: center;
}
.nav-link {
	margin: 0.5rem 1.8rem;
}
img {
	width: 6rem;
}
</style>
