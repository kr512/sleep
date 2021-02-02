<script>
	export let segment;
</script>

<style>
	nav {
		font-weight: 300;
		padding: 40px 10% 0px 10%;
		background: linear-gradient(0deg, rgba(0,0,0,0), rgba(0,0,0, 1) 80%) no-repeat;
		height: 100px;
		display: flex;
		justify-content: space-between;
	}
	@media(max-width:300px){
		nav {
			padding: 20px 5% 0px 5%;
		}
	}
	.logo {
		width: 130px;
		height: 65px;
		opacity: 1;
		transition: all 0.3s;
	}
	.logo:hover {
		opacity: .8;
	}
	.video {
		position: fixed;
		right: -2px; /* fix right white area */
		bottom: 0;
		min-width: 100%;
		min-height: 100%;
		z-index: -1;
		filter: blur(10px) brightness(0.5)
	}
	.background {
		position: fixed;
		right: 0;
		bottom: 0;
		min-width: 100%;
		min-height: 100%;
		z-index: -1;
		background-color: black;
	}
	.icons {
		margin-top: 20px;
	}
	.icon {
		color: white;
		width: 20px;
		height: 20px;
		padding: 10px;
		opacity: 0.4;
		transition: all 0.5s;
	}
	.icon-enabled, .icon-enabled:hover {
		opacity: 1;
	}
	.icon:hover {
		opacity: 0.8;
	}
	.no-selection {
		user-drag: none; 
		user-select: none;
		-moz-user-select: none;
		-webkit-user-drag: none;
		-webkit-user-select: none;
		-ms-user-select: none;
		cursor: default;
	}
</style>

<nav>
	<a href="/" class="no-selection">
		<img class="logo" src="/icon.png" alt="512.kr Sleep Icon">
	</a>
	<div class="icons no-selection">
		<a href="settings" class="no-selection">
			<img class="icon {segment==="settings" ? "icon-enabled" : ""}" src="cog-solid.svg" alt="Settings">
		</a>
		<a href="about" class="no-selection">
			<img class="icon {segment==="about" ? "icon-enabled" : ""}" src="ellipsis-v-solid.svg" alt="About">
		</a>
	</div>
</nav>


<div class="background"/>
<video class="video" width="1920" height="1080" autoplay muted loop>
	<source src="/background.mp4" type="video/mp4">
</video>