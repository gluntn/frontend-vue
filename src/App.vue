<template>
	<div id="app">
		<div id="menu-view">
			<div id="intro">
				<span>William</span>
				<span class="second">Slettvold</span>
				<span>Østensen</span>
			</div>
			<div id="brands">
				<router-link to="/twitter">
					<feather type="twitter" />
				</router-link>
				<router-link to="/linkedin">
					<feather type="linkedin" />
				</router-link>
				<router-link to="/github">
					<feather type="github" />
				</router-link>
			</div>
			<div id="links">
				<a href="#">Resumé</a>
				<a href="#">Projects</a>
			</div>
		</div>
	<div id="content-view">
		<router-view />
	</div>
</div>
</template>

<style lang="sass">
	@import '@/assets/style/all.sass'
	html
		background: $bg
		color: $fg
		font-family: 'Quicksand'
		letter-spacing: 0.02rem

	#menu-view
		#intro
			font-size: 3rem
			font-weight: 700
			span
				display: block
				&.second
					margin: .5rem 0
		#links
			font-size: 1.5rem
			margin-top: 2rem
			a
				color: $fg
			& a + a
				margin-left: 1rem
		#brands
			font-size: 2rem
			margin-top: 2rem
			a
				color: $fg
				text-decoration: none
				padding: .5rem
				margin-left: -.5rem
				&:hover > i
					transform: scale(1.3)
			& a + a
				margin-left: .5rem
				padding: .5rem
			i
				transition: 0.2s transform
	#content
			margin-top: 2rem
			font-size: 1.5rem
			font-weight: 200
			line-height: 1.75
			text-align: justify
			.highlight
				background: rgba(white, 0.1)
				padding: 0.5rem
			a
				color: $fg
				text-decoration: none
				background: rgba(white, 0.1)
				padding: .5rem
				transition: 0.2s background
				&:hover
					background: rgba(white, 0.15)

	@media only screen and (max-width: 699px)
		html
			font-size: 0.8em
	@media only screen and (min-width: 700px)
		html
			width: 75%
			margin: 2rem auto
	@media only screen and (min-width: 1100px)
		html
			width: 40%
			margin: 2rem auto
	@media only screen and (min-width: 1700px)
		html
			width: 35
			margin: 2rem auto
</style>
