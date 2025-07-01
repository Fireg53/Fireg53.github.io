<script>
	let { children } = $props();
</script>

<nav>
    <div class='bar short'>
      <a href="/">Home</a>
    </div>
    <div class='bar med'>
      <a href="/portfolio">Portfolio</a>
    </div>
    <div class='bar long'>
      <a href="/games">Games</a>
    </div>
</nav>

<div style="padding:20px">
    {@render children()}
</div>

<style>
 nav{
    /*border-style: dashed;
    border-color: red;*/
    position: absolute;
    left: 73%;
    font-family: "Fugaz One", sans-serif;
    font-weight: 400;
    font-style: normal;
    font-size: x-large;
    writing-mode: vertical-rl;
    display: flex;
    flex-direction: column-reverse;
    align-items: left;
    justify-content: right;
    row-gap: 2rem;
    margin-right: 1.2rem;
    margin-left: 1.2rem;
    margin-bottom: 1.2rem;
 }

 .bar{
    border-radius: 0px 0px 10px 10px;
    text-align: right;
    align-content: center;
    width: 3rem;
 }

 .short{
    background-color: #E6BCCD;
    height: 10rem;
 }

 .med{
    background-color: #D295BF;
    height: 17rem;
 }
 .long{
    background-color: #7E52A0;
    height: 24rem;
 }

 hr{
   width: 35rem;
   margin-right: 0px;
   margin-top: 0px;
   border-top: 5px solid #C163A4;
 }
 a{
    text-decoration: none;
    color: white;
    margin-bottom: 1rem;

 }
 p{
    color: #C163A4;
    margin: 0;
    font-size:xx-large;
 }
</style>