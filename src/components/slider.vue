<template>
    <div class="slider mt-3 absolute">
      <div class="slide-track -gap-20">
              <img class="slide h-16 w-auto" src="/src/assets/html5.png">
              <img class="slide h-16 w-auto" src="/src/assets/css.png">
              <img class="slide h-16 w-auto" src="/src/assets/javascript.png">
              <img class="slide h-16 w-auto" src="/src/assets/sass.png">
              <img class="slide h-16 w-auto" src="/src/assets/tailwind-css.png">
              <img class="slide h-16 w-auto" src="/src/assets/node-js.png">
              <img class="slide h-16 w-auto" src="/src/assets/graphql.png">
              <img class="slide h-16 w-auto" src="/src/assets/vuejs.png">
              <img class="slide h-16 w-auto" src="/src/assets/github.png">
      </div>
    </div>
</template>
<style scoped>
.slider {
 height: 5rem;
  width: 100%;
  display: grid;
  place-items: center;
  overflow: hidden;
}
.slider::before,
.slider::after{
  content:'';
  height:100%;
  width:25%;
  z-index:2;
  pointer-events:none;
}
.slider::before{
  left:0;
  top:0;
}
.slider::after{
  right:0;
  top:0;
  transform:rotateZ(180deg);
}

/*  IMPORTANT CODE BELOW */

.slide-track {
  width: calc(150px * 20);
  display: flex;
  animation: scroll 20s linear infinite;
  justify-content: space-between;



}


.slide-track2 {
  width: calc(150px * 15);
  display: flex;
  animation: scroll2 15s linear infinite;
  justify-content: space-between;
}

.slide {
  width: 3.4rem;
  aspect-ratio: 3/2;
  object-fit: contain;
  display: grid;
  place-items: center;
  transition:0.5s;
  cursor:pointer;
  mix-blend-mode:  color-burn;
}
.slide:hover{
  transform:scale(0.8)
}

@keyframes scroll {
  0% {
    transform: translateX(0px);
  }
  100% {
    transform: translateX(calc(-150px * 10));
  }
}

@keyframes scroll2 {
  0% {
    transform: translateX(0px);
  }
  100% {
    transform: translateX(calc(-150px * 5));
  }
}

@media screen and (max-width: 768px) {
  .slide-track {
    width: calc(80px * 20);
  }

  .slide-track2 {
    width: calc(80px * 15);
  }

  .slide {
    width: 80px;
  }

  @keyframes scroll {
    0% {
      transform: translateX(0px);
    }
    100% {
      transform: translateX(calc(-80px * 10));
    }
  }

  @keyframes scroll2 {
    0% {
      transform: translateX(0px);
    }
    100% {
      transform: translateX(calc(-80px * 5));
    }
  }
}
</style>