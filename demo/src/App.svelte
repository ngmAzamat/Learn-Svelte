<script></script>
<main>
  <div class="container">
    <div class="mini">
      <h1>Magic the gathering counter</h1>
      <button class="first">+</button>
      <button class="second">-</button>
      <button class="first">+</button>
      <button class="second">-</button>
      <button class="start">Start Game</button>
    </div>
  </div>
</main>
<style>
  .container {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    min-height: 100vh;
  }
  
  .mini {
    width: 80%;
    border: 1px solid grey;
    padding: 20px;
    background-color: wheat;
  }
  
  .first {
    width: 40px;
    border-radius: 3px;
    background-color: seagreen;
    color: white;
    font-size: 20px;
    font-family: monospace;
    border: none;
    font-weight: bold;


  }
  
  .second {
    border-radius: 3px;
    font-size: 20px;
    font-family: monospace;
    font-weight: bold;
    width: 40px;
    background-color: brown;
    color: white;
    border: none;
  }
  
  .start {
    width: 100%;
    padding: 20px;
    background-color: sandybrown;
    color: black;
    font-size: 20px;
    font-family: monospace;
    font-weight: bold;
    border: 1px solid salmon;
  }
</style>
