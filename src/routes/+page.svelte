<div class="canvas">
  <div class="poly bg-cyan-950"></div>
  <div class="poly bg-green-950"></div>
  <div class="poly bg-red-950"></div>
  <div class="poly bg-amber-200"></div>
  <div class="poly bg-pink-700"></div>
</div>
<div class="canvas">
  <div class="poly bg-cyan-950"></div>
</div>
<div class="canvas">
  <div class="frame bg-amber-950"></div>
  <div class="frame bg-blue-400"></div>
  <div class="frame bg-yellow-600"></div>
  <div class="frame bg-green-900"></div>
  <div class="frame bg-red-900"></div>
</div>
<div class="canvas">
  <div class="poly-test bg-cyan-200">
    <div class="innie bg-yellow-600"></div>
  </div>
</div>

<style>
  .poly {
    --width: 250px;
    --slant-offest: 50px;

    width: var(--width);
    clip-path: polygon(
      var(--slant-offest) 0%, 
      100% 0%,
      calc(100% - var(--slant-offest)) 100%,
      0% 100%
    );

    margin-left: calc(-1 * var(--slant-offest));
    transition: width .5s ease;

    &:hover {
      --width: 500px;
      transition: width .2s ease;
    }

    &:first-child {
      margin-left: 0;
    }
  }

  .poly2 {
    width: 250px;
    clip-path: polygon(20% 0%, 100% 0%, 80% 100%, 0% 100%);
    margin-left: -50px;
    
    transition: width .5s ease, margin-left .5s ease;
    &:hover {
      width: 500px;
      /* clip-path: polygon(20% 0%, 100% 0%, 80% 100%, 0% 100%); */
      margin-left: -50px;
      transition: width .2s ease, margin-left .5s ease;
    }

    &:first-child {
      margin-left: 0;
    }
  }


  .canvas {
    border: 1px solid salmon;
    width: 90vw;
    height: 40vh;
    display: flex;
    /* gap: 50px; */
    justify-content: center;
  }

  .frame {
    border: 1px solid bisque;
    width: 15vw;
    height: 100%;
    transition: width .5s ease;

    &:hover {
      width: 30vw;
      transition: width .2s ease;
    }
  }

  .poly-test {
    position: relative;
    align-self: center;
    width: 600px;
    height: 300px;
    clip-path: polygon(10% 0%, 100% 0%, 90% 100%, 0% 100%);
  }

  .innie {
    position: absolute;
    width: 590px;
    height: 290px; 
    clip-path: polygon(10% 0%, 100% 0%, 90% 100%, 0% 100%);
    top: 5px;
    left: 5px;
  }

</style>