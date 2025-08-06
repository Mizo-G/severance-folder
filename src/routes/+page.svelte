<div class="canvas">
  <div class="poly bg-cyan-950"></div>
  <div class="poly bg-green-950"></div>
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
    width: 250px;
    clip-path: polygon(20% 0%, 100% 0%, 80% 100%, 0% 100%);
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