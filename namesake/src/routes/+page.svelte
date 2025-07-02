<script>
	function openInNewTab(url) {
		window.open(url, '_blank').focus();
	}
</script>

<br>
<br>
<header>
	<h1>Iyan</h1>
	<h1>Syeed-Miller</h1>
</header>
<br>
<div class="links">
	<button onclick={openInNewTab("https://github.com/Fireg53")}><i class="fab fa-github"></i><span>@Fireg53</span></button>
	<button onclick={openInNewTab("https://www.youtube.com/@fireg5355")}><i class="fab fa-youtube"></i> <span>@fireg5355</span></button>
	<button onclick={openInNewTab("https://www.instagram.com/iyan.in3d/")}><i class="fab fa-square-instagram"></i> <span>@iyan.in3d</span></button>
	<button onclick={openInNewTab("mailto:iyansyeedmiller@gmail.com")}><i class="fas fa-envelope"></i> <span>@iyansyeedmiller@gmail.com</span></button>
</div>
<div class="resume">
	<iframe
	src="Resume.pdf#toolbar=0"
	width= 100%
	height= 100%
	style="border:none"
	title="Non-downloadable PDF Viewer"
	></iframe>
</div>

<style>
	h1{
		font-family: "Climate Crisis", sans-serif;
		font-optical-sizing: auto;
		font-weight: 400;
		font-style: normal;
		font-variation-settings:
			"YEAR" 1979;
		color: #29274C;
		font-size: 6.5vw;
		line-height: 2rem;
		margin-left: 5%;
		margin-right: 10%;
		margin-top: 4rem;
	}
	.links{
		display: flex;
		column-gap: 2rem;
		color: #29274C;
		margin-left: 5%;
	}
	.resume{
		display: flex;
		direction: column;
		justify-content: center;
		align-items: center;
		padding: 20px;
		margin-top: 5rem;
		margin-right:40%;
		background-image: linear-gradient( #E6BCCD, #D295BF, #7E52A0);
		width: 55vw;
		height: 70vw;
		border-radius: 20px;
		margin-left: 5%;
	}
</style>
