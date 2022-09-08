<template>
	<div class="popup">
		<div class="popup__wrap">
			<div class="popup__top-content">
				<h2 class="popup__title">Glückwunsch!<br>lhr Gewinn ist</h2>
			</div>
			<div class="popup__main-content">
				<h2 class="popup__winners">1.500 eur und<br>270 freispiele</h2>
				<img src="@/assets/images/money_icon.png" alt="Money">
				<button class="popup__btn">erhalten</button>
			</div>
		</div>
	</div>
</template>

<script>
export default {
}
</script>

<style lang="scss" scoped>
.popup {
	display: none;
	z-index: 101;
	background: #fff;
	width: 350px;
	text-align: center;
	position: fixed;
	top: 14%;
	border-radius: 7px;
	&__wrap {
	}
	&__top-content {
		padding-top: 30px;
		border-radius: 7px;
		background: blue;
		position: relative;
		&::before {
		content: "";
		position: absolute;
		left: 0;
		bottom: 0;
		right: 0;
		background-repeat: repeat;
		height: 10px;
		background-size: 20px 20px;
		background-image:
    radial-gradient(circle at 10px -5px, transparent 12px, #fff 13px);
		}
		&::after{
		content: "";
		position: absolute;
		left: 0;
		bottom: 0;
		right: 0;
		background-repeat: repeat;
		height: 15px;
		background-size: 40px 20px;
		background-image:
    radial-gradient(circle at 10px 15px, #fff 12px, transparent 13px);
		}
	}
	&__title {
		font-size: 35px;
		color: yellow;
		padding-bottom: 20px;
	}
	&__main-content {
		text-align: center;
		padding-bottom: 20px;
		img {
			width: 150px;
			padding-bottom: 10px;
		}
	}
	&__winners {
		font-size: 25px;
		font-weight: 800;
		padding: 15px;
		color: red;
		text-transform: uppercase;
	}
	&__btn {
		color: #fff;
		background: rgb(53,167,110);
		text-transform: uppercase;
		padding: 25px 33px;
		font-size: 30px;
		border-radius: 5px;
		outline: none;
		border: none;
		box-shadow: 0 -6px green inset;
		display: block;
		margin: 0 auto;
		font-weight: 700;
	}
}
</style>