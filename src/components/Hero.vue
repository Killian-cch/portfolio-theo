<template>
	<div class="hero">
		<div>
		</div>
		<div class="title">
			<div>
				<div class="name">théo renaux</div>
				<div class="job">graphiste<br>ui ux designer</div>
			</div>
		</div>
	</div>
</template>

<style lang="sass" scoped>
	@import "@/assets/breakpoints.sass"

	.hero
		display: flex
		flex-flow: row nowrap
		border-top: solid 1px #313131
		border-bottom: solid 1px #313131
		height: calc( 100vh - 103px )
		@include breakpoint($m-screen)
			border: none
		@include breakpoint($s-screen)
			padding-top: 70px
			height: calc( 100vh - 70px )

		> div:first-child
			flex-grow: 3
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

		.name
			display: inline
			text-align: left
			font-size: 5vw
			font-weight: 100
			text-transform: capitalize
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
			@include breakpoint($m-screen)
				font-size: 9vw
			@include breakpoint($s-screen)
				font-size: 10vw
</style>