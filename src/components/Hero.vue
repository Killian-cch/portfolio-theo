<script setup>
	import scrollWhite from "@/assets/images/scroll_blanc.json";
</script>

<template>
	<div class="hero">
		<div>
		</div>
		<div class="title">
			<div>
				<div class="name">théo renaux</div>
				<div class="job">graphiste<br>ui ux designer</div>
			</div>
			<div class="scroll">
				<Vue3Lottie class="" :animationData="scrollWhite" />
			</div>
		</div>
	</div>
</template>

<style lang="sass" scoped>
	@import "@/assets/styles/breakpoints.sass"

	.hero
		display: flex
		margin-top: 140px
		flex-flow: row nowrap
		margin-bottom: 4rem
		border-bottom: solid 1px #313131
		border-top: solid 1px #313131
		@include breakpoint($m-screen)
			border: none
			height: calc(100vh - 140px)
			margin-bottom: 0
		@include breakpoint($s-screen)
			padding-top: 70px
			height: calc(100vh - 70px)
			margin-top: 70px
		> div:first-child
			flex-grow: 1
			border-right: solid 1px #565656
			@include breakpoint($m-screen)
				display: none
				border: none
		.title
			display: flex
			flex-flow: column nowrap
			justify-content: center
			align-items: center
			flex-grow: 1
			margin: calc(5vw + 5rem) 0

			.name
				display: inline
				text-align: left
				font-size: 5vw
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
				font-size: 7vw
				text-transform: uppercase
				font-family: Stylish Delight
				white-space: nowrap
				margin-top: 1rem
				@include breakpoint($m-screen)
					font-size: 9vw
				@include breakpoint($s-screen)
					font-size: 10vw
		.scroll
			margin-left: auto
			margin-right: 2vw
			display: flex
			position: relative
			@include breakpoint($m-screen)
				margin: 0
				z-index: 0
			> *
				width: 400px
</style>