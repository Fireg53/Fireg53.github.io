<script>
	function openInNewTab(url) {
		window.open(url, '_blank').focus();
	}
</script>
<div class='page'>
	<br>
	<br>
	<header>
		<h1>Iyan</h1>
		<h1>Syeed-Miller</h1>
	</header>
	<br>
	<div class="links">
		<button onclick={openInNewTab("https://github.com/Fireg53")} class="gradient"><i class="fab fa-github"></i><span>Fireg53</span></button>
		<button onclick={openInNewTab("https://www.youtube.com/@fireg5355")} class="gradient"><i class="fab fa-youtube"></i> <span>Fireg5355</span></button>
		<button onclick={openInNewTab("https://www.instagram.com/iyan.in3d/")} class="gradient"><i class="fab fa-instagram"></i>Iyan.in3d</button>
		<button onclick={openInNewTab("mailto:iyansyeedmiller@gmail.com")} class="gradient"><i class="fas fa-envelope"></i> <span>Iyansyeedmiller@gmail.com</span></button>
	</div>
	<div class="resume_container">
		<div class="resume">
			<span class='label'><p>Resume</p><button class='download'><i class="fas fa-download"></i></button></span>
			<img src="Resume.png" alt='Resume' style='width:100%; height:100%; border-radius:6px;'>
		</div>
	</div>
</div>

<style>
	.page{
		padding: 20px;
	}
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
	.resume_container{
		display: flex;
		justify-content: center;
	}
	.resume{
		display: flex;
		flex-direction: column;
		padding: 20px;
		margin-top: 5rem;
		background-image: linear-gradient( #E6BCCD, #D295BF, #7E52A0);
		width: 55vw;
		height: 70vw;
		border-radius: 20px;
	}
	.label{
		padding-left: 2vw;
		padding-right: 2vw;
		display: flex;
		flex-direction: row;
		justify-content: space-between;
		align-items: center;
		color: white;
		font-family: "Fugaz One", sans-serif;
		font-weight: 400;
		font-style: normal;
		font-size: 1.5vw;
		line-height: 0.2vw;

	}
	.download {
		background-color:#E6BCCD;
		border: 0;
		color: white;
		cursor: pointer;
	}
	.gradient {
	align-items: center;
	background-image: linear-gradient(144deg,#E6BCCD, #D295BF 20%, #7E52A0);
	border: 0;
	border-radius: 8px;
	box-shadow: rgba(151, 65, 252, 0.2) 0 15px 30px -5px;
	box-sizing: border-box;
	color: #FFFFFF;
	display: flex;
	font-family: Phantomsans, sans-serif;
	font-size: 1em;
	justify-content: center;
	column-gap: 0.5em;
	max-width: 30%;
	min-width: 2em;
	padding: 8px 12px; 
	text-decoration: none;
	user-select: none;
	touch-action: manipulation;
	white-space: nowrap;
	cursor: pointer;
	transition: box-shadow ease 0.5s;
	}

	.gradient:active,
	.gradient:not([disabled]):hover {
		box-shadow:  -.125rem -.125rem 0.5rem #E6BCCD, .125rem .125rem 0.5rem #c085ee;
	}
</style>