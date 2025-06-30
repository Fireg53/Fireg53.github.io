<script>
	let { children } = $props();
</script>

<nav>
   <div id='links'>
      <a href="/">Home</a>
      <p>✦</p>
      <a href="/portfolio">Portfolio</a>
      <p>✦</p>
      <a href="/games">Games</a>
   </div>
   <hr>
</nav>

{@render children()}

<style>
 nav{
    /*border-style: dashed;
    border-color: red;*/
    font-family: "Fugaz One", sans-serif;
    font-weight: 400;
    font-style: normal;
    font-size: x-large;
 }

 #links{
    display: flex;
    align-items: center;
    justify-content: right;
    column-gap: 3rem;
    margin-top: 10px;
    margin-right: 25px;
    margin-left: 25px;
    /*box-shadow: inset 0 -4px;*/
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
 }
 p{
    color: #C163A4;
    margin: 0;
    font-size:xx-large;
 }
</style>