<script>
  import { fade } from 'svelte/transition';

  let gameshow = {
    title: 'Block Puzzle',
    link: 'https://classlive-docs.vercel.app/blockpuzzle',
    image: 'https://classlive.vercel.app/block.svg'
  };
</script>

<svelte:head>
  <title>Block Puzzle Challenge</title>
  <meta name="description" content="Block Puzzle Challenge - An exciting game show based on the block puzzle game!" />
</svelte:head>

<div class="text-column">
  <h1>Block Puzzle Challenge</h1>

  <p>
    Welcome to the Block Puzzle Challenge! Compete in this thrilling game show based on the classic block puzzle game.
  </p>
</div>

<div class="grid">
  <a href={gameshow.link} target="_blank" class="cell">
    <div class="cell-inner" transition:fade>
      <div id={'bg-' + gameshow.title} class="bg">
        <img src={gameshow.image} alt="Block Puzzle Challenge Image" />
      </div>
      <div class="content">
        <h2>{gameshow.title}</h2>
        <p>Compete in a thrilling block puzzle game show!</p>
      </div>
    </div>
  </a>
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
