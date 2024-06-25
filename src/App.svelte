<script>
  import { onMount } from "svelte";

  let canvas;
  let ctx;

  onMount(() => {
    ctx = canvas.getContext("2d");

    // Draw a filled rectangle
    ctx.fillStyle = "green";
    ctx.fillRect(10, 10, 100, 100);

    // Draw a rectangle outline
    ctx.strokeStyle = "blue";
    ctx.strokeRect(130, 10, 150, 120);

    // Draw a filled rectangle
    ctx.fillStyle = "green";
    ctx.fillRect(300, 10, 200, 100);
    // Clear a rectangle area
    ctx.clearRect(380, 30, 50, 50);

    // Draw a line
    ctx.beginPath();
    ctx.moveTo(20, 190);
    ctx.lineTo(190, 190);
    ctx.lineTo(190, 250);
    ctx.lineTo(120, 250);
    ctx.lineTo(120, 280);
    ctx.lineTo(90, 280);
    ctx.lineTo(90, 250);
    ctx.lineTo(20, 250);
    ctx.closePath();
    ctx.stroke();

    // Draw a line triangle
    ctx.beginPath();
    ctx.moveTo(250, 190);
    ctx.lineTo(410, 190);
    ctx.lineTo(410, 260);
    ctx.closePath();
    ctx.stroke();

    // Draw a circle
    ctx.beginPath();
    ctx.arc(300, 300, 60, 0, Math.PI * 2, false);
    ctx.fillStyle = "purple";
    ctx.fill();
    ctx.stroke();

    // Draw a bangladesh flag
    ctx.fillStyle = "#086F54";
    ctx.fillRect(50, 450, 600, 350);
    ctx.beginPath();
    ctx.arc(300, 625, 125, 0, Math.PI * 2, false);
    ctx.fillStyle = "#F43147";
    ctx.fill();

    ctx.strokeStyle = "blue";
    ctx.strokeRect(40, 430, 10, 820);

    ctx.fillStyle = "black";
    ctx.fillRect(40, 430, 10, 820);
    ctx.strokeRect(10, 1250, 80, 40);
    // ctx.fill();
    ctx.fillStyle = "black";
    ctx.fillRect(10, 1250, 80, 40);

    // Draw text
    ctx.font = "30px Arial";
    ctx.fillStyle = "black";
    ctx.fillText("Hello Canvas", 10, 350);
    ctx.strokeStyle = "red";
    ctx.strokeText("Hello Canvas", 10, 400);
  });
</script>

<canvas
  bind:this={canvas}
  width="1000"
  height="2000"
  style="border:1px solid #000000;"
></canvas>
