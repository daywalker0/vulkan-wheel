<template>
	<div class="wheel">
		<div class="wheel__wrap">
			<img class="wheel__img" src="@/assets/images/wheel-spinner.png" alt="Wheel">
			<img class="wheel__pointer" src="@/assets/images/pointer.png" alt="Pointer">
			<div class="wheel__btn-block"><a @click.prevent="rotateWheel" class="wheel__btn">spin</a></div>
		</div>
	</div>
</template>

<script>
export default {
methods: {
		rotateWheel() {
			const btn = document.querySelector('.wheel__btn');
			const spinner = document.querySelector('.wheel__img');
			const popup = document.querySelector('.popup');
			const pointer = document.querySelector('.pointer');
			btn.addEventListener('click', spinner.classList.add('rotate'))
			setTimeout(() => {
				popup.classList.add('open')
			}, 5000);
		}
	}
}
</script>

<style lang="scss">

.wheel {
		position: relative;
		bottom: 40px;
		left: 0;
	&__img {
		max-width: 900px;
		animation-name: spinner;
		animation-duration: 5s;
		animation-iteration-count: infinite;
		animation-timing-function: ease-in;
		animation-fill-mode: forwards;
	}
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
		&__btn-block {
			background: url('@/assets/images/ball3.png');
			background-size: cover;
			width: 64px;
			height: 64px;
			z-index: 99;
			position: absolute;
			left: 44%;
			top: 44%;
			text-align: center;
			vertical-align: middle;
		}
		&__btn {
			display: inline-block;
			margin-top: 22px;
			font-size: 20px;
			color: #fff;
			text-transform: uppercase;
			background: none;
			border: none;
			cursor: pointer;
		}
	@keyframes spinner {
		0% {
				transform:rotate(0deg);
		}
		18% {
				transform:rotate(5deg);
		}
		36% {
				transform:rotate(0deg);
		}
		44% {
				transform:rotate(5deg);
		}
		62% {
				transform:rotate(0deg);
		}
		80% {
				transform:rotate(5deg);
		}
		100% {
				transform:rotate(0deg);
		}
	}
		.rotate {
		animation-name: rotation;
    animation-duration: 5s;
    animation-iteration-count: 1;
    animation-timing-function: ease;
		animation-fill-mode: forwards;
	}
	@keyframes rotation {
    0% {
        transform:rotate(0deg);
    }
    85% {
        transform:rotate(1050deg);
    }
		100% {
				transform:rotate(1040deg);
		}
	}
	.open {
		display: block;
	}
}
@media (max-width: 768px) {
	.wheel {
		&__img {
			max-width: 540px;
		}
	}
}
@media (max-width: 374px) {
	.wheel {
		&__img {
			max-width: 468px;
		}
		&__pointer {
			left: 41%;
			top: 42%;
		}
		&__btn-block {
			left: 43%;
			top: 43%;
		}
		&__btn {
			margin-top: 20px;
		}
	}
}

</style>