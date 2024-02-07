<script>
  const gameUrl = "https://classlive-docs.vercel.app/blockpuzzle";
</script>

<style>
  main {
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
    text-align: center;
  }

  h1 {
    font-size: 2.5rem;
    margin-bottom: 20px;
  }

  p {
    font-size: 1.2rem;
    line-height: 1.5;
    margin-bottom: 30px;
  }

  .game-link {
    margin-top: 50px;
  }

  .game-link img {
    width: 300px;
    height: auto;
    cursor: pointer;
    border-radius: 10px;
    box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease;
  }

  .game-link img:hover {
    transform: translateY(-5px);
  }

  .play-link {
    display: block;
    margin-top: 20px;
    font-size: 1.1rem;
    color: #333;
    text-decoration: none;
  }

  .play-link:hover {
    color: #555;
  }
</style>

<main>
  <h1>Welcome to Block Puzzle</h1>
  <p>Block Puzzle is a fun and addictive puzzle game that challenges your spatial awareness and problem-solving skills. Drag and drop blocks onto the grid to create full lines and clear them from the board. Can you beat your high score?</p>
  <div class="game-link">
    <a href={gameUrl} target="_blank" rel="noopener">
      <img src="https://classlive.vercel.app/block.svg" alt="Block Puzzle" />
    </a>
    <a class="play-link" href={gameUrl} target="_blank" rel="noopener">Click here to play</a>
  </div>
</main>
