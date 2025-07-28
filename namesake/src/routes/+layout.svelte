<script>
   import { onNavigate } from "$app/navigation";
   import { page } from '$app/stores';
   import { derived } from 'svelte/store';

  // Optional: make a derived store if you only need the pathname
  const currentPath = derived(page, $page => $page.url.pathname);

	let { children } = $props();

   onNavigate((navigation) => {
      if (!document.startViewTransition) return;

      return new Promise((resolve) => {
         document.startViewTransition(async () => {
            resolve();
            await navigation.complete;
         });
      });
   });
</script>

<nav>
   <div class='bar short'>
      {#if currentPath === '/'}
         <span class="active">Home</span>
      {:else}
         <a href="/">Home</a>
      {/if}
   </div>

   <div class='bar med'>
      {#if currentPath === '/portfolio'}
         <span class="active">Portfolio</span>
      {:else}
         <a href="/portfolio">Portfolio</a>
      {/if}
   </div>

   <div class='bar long'>
      {#if currentPath === '/games'}
         <span class="active">Games</span>
      {:else}
         <a href="/games">Games</a>
      {/if}
   </div>
</nav>

<div>
    {@render children()}
</div>

<style>

 nav{
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
    view-transition-name: header;
 }

 .bar{
    border-radius: 0px 0px 10px 10px;
    text-align: right;
    align-content: center;
    width: 3rem;
    position: relative;
    top: 0;
 }

 .short{
    background-color: #E6BCCD;
    box-shadow: 1px 1px 4px #c787a1;
    height: 10rem;
    transition: height ease 0.5s;
 }
 .short:not([disabled]):hover{
    height: 10.4rem;
 }

 .med{
    background-color: #D295BF;
    box-shadow: 1px 1px 4px rgb(148, 86, 110);
    height: 17rem;
    transition: height ease 0.5s;
 }
 .med:not([disabled]):hover{
    height: 17.4rem;
 }

 .long{
    background-color: #7E52A0;
    box-shadow: 1px 1px 4px #2e1542;
    height: 24rem;
    transition: height ease 0.5s;
 }
 .long:not([disabled]):hover{
    height: 24.4rem;
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
 
/*Page Transitions*/

 @keyframes fade-in {
	from {
		opacity: 0;
	}
}

@keyframes fade-out {
	to {
		opacity: 0;
	}
}

@keyframes slide-from-top {
	from {
		transform: translateY(-100vh);
	}
}

@keyframes slide-to-bottom {
	to {
		transform: translateY(-30px);
	}
}

@keyframes spin {
   from {
      transform: rotate(20deg);
   }
}


:root::view-transition-old(root) {
  z-index: 1; /* Behind the new page */
  animation: 3000ms;
}

:root::view-transition-new(root) {
   z-index: 2;
	animation:
      1000ms cubic-bezier(0.4, 0, 0.2, 1) both spin,
		210ms cubic-bezier(0, 0, 0.2, 1) 90ms both fade-in,
		1000ms cubic-bezier(0.4, 0, 0.2, 1) both slide-from-top;
}
</style>