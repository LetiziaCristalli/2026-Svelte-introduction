<script>
    import{onMount} from "svelte";

    let size = $state(50);
    let color = $state('#ff0000');

    let canvas

    $effect (() => {
        const context = canvas.getContext('2d');
        context.clearRect(0, 0, canvas.width, canvas.height);


        context.fillStyle = color;
        context.fillRect(0, 0, size, size);
    });

  </script>
  <h3>Canvas Square</h3>
  <article>
    <canvas bind:this={canvas} width="100" height="100"></canvas>
  
    <nav>
      <label>
          size: <input type="range" bind:value={size}>
      </label>
  
      <label>
          color: <input type="color" bind:value={color}>
      </label>
    </nav>
  </article>
  <style>
    article {
      display: flex;
      gap: 1 em;
      align-items: end;
    }
  
    canvas {
      border: 1px solid black;
    }
  
    nav {
      display: flex;
      flex-direction: column;
      gap: 1 em;
    }
  </style>