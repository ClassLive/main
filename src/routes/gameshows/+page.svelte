<script>
	import { fade } from 'svelte/transition';
  
	let gameshows = [
	  { title: 'Show 1', link: '/show1', image: 'https://via.placeholder.com/640x360.png?text=Game+1' },
	  { title: 'Show 2', link: '/show2', image: 'https://via.placeholder.com/640x360.png?text=Game+2' },
	  // add more gameshows here
	];
  </script>
  
  <svelte:head>
	<title>Gameshows</title>
	<meta name="description" content="Gameshows" />
  </svelte:head>
  
  <div class="text-column">
	<h1>Gameshows</h1>
  
	<p>
	  We currently do not have any finished gameshows, check back soon!
	</p>
  </div>
  
  <div class="grid">
	{#each gameshows as show}
	  <a href={show.link} class="cell">
		<div class="cell-inner" transition:fade>
		  <div id={'bg-' + show.title} class="bg">
			<img src={show.image} alt="Game Image" />
		  </div>
		  <div class="content">
			<h2>{show.title}</h2>
		  </div>
		</div>
	  </a>
	{/each}
  </div>
  
  <style>
	.text-column {
	  max-width: 800px;
	  margin: 0 auto;
	}
  
	.grid {
	  display: grid;
	  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
	  grid-gap: 20px;
	  padding: 20px;
	}
  
	.cell {
	  display: block;
	  position: relative;
	  overflow: hidden;
	  color: white;
	  text-decoration: none;
	}
  
	.cell-inner {
	  position: relative;
	  z-index: 2;
	  transition: opacity 0.3s;
	}
  
	.cell-inner:hover {
	  opacity: 1;
	}
  
	.bg {
	  position: absolute;
	  top: 0;
	  left: 0;
	  width: 100%;
	  height: 100%;
	}
  
	.content {
	  position: absolute;
	  bottom: 0;
	  left: 0;
	  width: 100%;
	  padding: 20px;
	  background-image: linear-gradient(to bottom, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8));
	  z-index: 3;
	}
  
	h2 {
	  margin: 0;
	}
  </style>
  