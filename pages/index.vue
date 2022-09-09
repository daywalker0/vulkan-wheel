<template>
	<section class="s-wheel-page">
		<div class="wheel-page__container">
			<Logo />
			<Wheel />
			<Popup />
		</div>
	</section>
</template>

<script>
export default {
  name: 'IndexPage',
}
</script>

<style lang="scss">
.s-wheel-page {
	min-height: 100vh;
	background: url('../assets/images/decor_grass_des.jpg');
	background-size: 100%;
	background-repeat: no-repeat;
}
.wheel-page__container {
	display: flex;
	flex-direction: column;
	align-items: center;
	overflow: hidden;
	padding: 0 10px;
	position: relative;
}
@media (max-width: 768px) {
	.s-wheel-page {
		min-height: 100vh;
		background: url('../assets/images/decor_grass_mob.jpg');
		background-size: 100%;
	}
}
</style>
