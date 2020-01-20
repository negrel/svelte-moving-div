<div
  bind:this={movingDiv}
  on:mouseenter={trackMouse}
  on:mousemove={updatePosition}
  on:mouseleave={resetPosition}
  class="moving-div"
>
  <div bind:this={innerDiv} class="inner-div">
    <slot />
  </div>
</div>

<script>
let mouse = {
  x: 0,
  y: 0
};

let movingDiv,
  innerDiv

// Track the mouse when it hover the moving div
function trackMouse() {
  movingDiv.addEventListener('mousemove', setMouse);
}

function setMouse(event) {
  mouse.x = event.clientX;
  mouse.y = event.clientY;
}

function updatePosition() {
  if (isHover(movingDiv)) {
    const { top, left } = movingDiv.getBoundingClientRect(),
      centerX = left + movingDiv.offsetWidth / 2,
      centerY = top + movingDiv.offsetHeight / 2,
      elPosX = (mouse.x - centerX) / 2,
      elPosY = (mouse.y - centerY) / 2;

    innerDiv.style.transform = `translate3d(${elPosX}px, ${elPosY}px, 0)`;
    requestAnimationFrame(updatePosition);
  } else {
    resetPosition();
  }
}
// Reset the moving div postion.
function resetPosition() {
  movingDiv.removeEventListener('mousemove', setMouse);
  innerDiv.style.transform = 'translate3d(0, 0, 0)';
}

// Return if the given element is hovered
function isHover(e) {
  return e.parentElement.querySelector(':hover') === e;
}

</script>

<style>
.moving-div {
  width: fit-content;
  cursor: pointer;
}

.moving-div > .inner-div {
  position: relative;
  pointer-events: none;
  transform: translate3d(0, 0, 0);
  transition: transform 1s;
}
</style>