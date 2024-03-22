<script setup>
	import scrollWhite from "@/assets/images/scroll_blanc.json";
</script>

<template>
	<div class="hero">
		<div class="title">
			<div>
				<div class="name">théo renaux</div>
				<div class="job">graphiste<br>ui ux designer</div>
			</div>
		</div>
		<!-- <Vue3Lottie class="scroll" :animationData="scrollWhite" /> -->
	</div>
</template>

<style lang="sass" scoped>
	@import "@/assets/styles/breakpoints.sass"

	.hero
		position: relative
		padding-top: 8.75rem
		margin-bottom: 4rem
		height: 100vh //8.75rem
		border-bottom: solid 1px #313131
		@include breakpoint($s-screen)
			padding-top: 70px
			margin-bottom: 0
			border: none
		&::before
			content: ''
			display: block
			height: auto
			width: 100%
			border-top: solid 1px #313131
		.title
			position: absolute
			right: 0
			border-left: solid 1px #565656
			display: flex
			flex-flow: column nowrap
			justify-content: center
			align-items: center
			width: 80%
			height: calc(100% - 8.75rem - 1px)
			padding: 0 10%
			@include breakpoint($s-screen)
				height: calc(100% - 71px)
				width: 100%
				border: none

			.name
				display: inline
				text-align: left
				font-size: 3.5rem
				font-weight: 200
				text-transform: capitalize
				margin-bottom: 3rem
				@include breakpoint($m-screen)
					font-size: 6vw
				@include breakpoint($s-screen)
					font-size: 7vw

			.job
				width: fit-content
				text-align: right
				font-size: 7rem
				text-transform: uppercase
				font-family: Stylish Delight
				white-space: nowrap
				margin-top: 1rem
				@include breakpoint($m-screen)
					font-size: 9vw
				@include breakpoint($s-screen)
					font-size: 10vw
		// // .scroll
		// 	position: absolute
		// 	right: 0
		// 	bottom: 0
		// 	transform: translate(-50%, -50%)
		// 	width: 330px
</style>