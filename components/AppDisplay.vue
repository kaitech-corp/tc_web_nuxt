<template>
  <img class="tc-logo" alt="TC Logo" src="@/assets/images/web1.png" />
</template>

<style>
.tc-logo {
  max-width: 636px;
  height: 750px;
  transform: rotateY(560deg);
  animation: turn 3.5s ease-out forwards 1s;
}

@keyframes turn {
  100% {
    transform: rotateY(0deg);
  }
}
</style>