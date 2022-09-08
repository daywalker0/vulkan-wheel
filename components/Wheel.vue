<template>
	<div class="wheel">
		<div class="wheel__wrap">
			<img class="wheel__img" src="@/assets/images/wheel-spinner.png" alt="Wheel">
			<img class="wheel__pointer" src="@/assets/images/pointer.png" alt="Pointer">
			<div class="wheel__btn"><button @click="showPopup">spin</button></div>
		</div>
		<!-- <Popup
			v-if="isPopVisible"
		/> -->
	</div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
@media (max-width: 768px) {
	.wheel {
		position: relative;
		bottom: 40px;
		left: 0;
		&__wrap {
			position: relative;
		}
		&__img {
			max-width: 540px;
		}
		&__pointer {
			position: absolute;
			width: 100px;
			left: 42%;
			top: 43%;
		}
		&__btn {
			background: url('@/assets/images/ball2.png');
			background-size: cover;
			width: 64px;
			height: 64px;
			z-index: 99;
			position: absolute;
			left: 44%;
			top: 44%;
			text-align: center;
			vertical-align: middle;
			button {
				display: inline-block;
				margin-top: 22px;
				font-size: 20px;
				color: #fff;
				text-transform: uppercase;
				background: none;
				border: none;
				cursor: pointer;
			}
		}
	}
}

</style>