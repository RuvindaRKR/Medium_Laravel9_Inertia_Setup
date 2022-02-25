<template>
  <div class="body1">
    <div class="wrapper">
      <p class="dream">
        <span>C</span>
        <span>h</span>
        <span>r</span>
        <span>i</span>
        <span>s</span>
        <span>t</span>
        <span>i</span>
        <span>n</span>
        <span>a</span>
      </p>
      <p class="dangerously">
        <span>d</span>
        <span>a</span>
        <span>v</span>
        <span>i</span>
        <span>d</span>
      </p>
    </div>
  </div>
</template>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@1,700&family=Roboto:ital,wght@1,100&display=swap");

$orange: #df725d;
$white: #f5f5f5;

.body1 {
  margin: 0;
  padding: 0;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  overflow: hidden;
}

.wrapper {
  &:hover {
    p span {
      animation: smoke 1.75s ease-in forwards;
    }
  }
}

p {
  opacity: 0;
  margin: 0;
  font-style: italic;
  color: $white;
  filter: blur(0.02vmin);
  animation: fade-in 1s ease-in-out forwards;
  text-shadow: 0 0 2vmin $orange;

  span {
    display: inline-block;
  }

  // Dream
  &.dream {
    font-size: 24vmin;
    font-family: "Playfair Display", serif;
    font-weight: 700;
    margin: -10% 0 -5%;
    animation-delay: 1s;

    span {
      margin-left: 0%;

      &:nth-child(1) {
        animation-delay: 0.6s;
      }

      &:nth-child(2) {
        animation-delay: 1s;
      }

      &:nth-child(3) {
        animation-delay: 0.8s;
      }

      &:nth-child(4) {
        animation-delay: 1.4s;
      }

      &:nth-child(5) {
        animation-delay: 1.2s;
      }
    }
  }

  // Dangerously
  &.dangerously {
    font-size: 9vmin;
    font-family: "Roboto", sans-serif;
    font-weight: 100;
    text-transform: uppercase;
    padding-left: 18%;
    animation-delay: 1.5s;

    span {
      margin-left: -1.5%;

      &:nth-child(1) {
        animation-delay: 1.4s;
      }

      &:nth-child(2) {
        animation-delay: 1.2s;
      }

      &:nth-child(3) {
        animation-delay: 1.6s;
      }

      &:nth-child(4) {
        animation-delay: 1.8s;
      }

      &:nth-child(5) {
        animation-delay: 2s;
      }

      &:nth-child(6) {
        animation-delay: 2.4s;
      }

      &:nth-child(7) {
        animation-delay: 2.2s;
      }

      &:nth-child(8) {
        animation-delay: 2.6s;
      }

      &:nth-child(9) {
        animation-delay: 2.8s;
      }

      &:nth-child(10) {
        animation-delay: 3.2s;
      }

      &:nth-child(11) {
        animation-delay: 3s;
      }
    }
  }
}

@keyframes smoke {
  0% {
    transform: rotate(0deg) translate3d(0%) skew(0deg) scale(1);
    opacity: 1;
    filter: blur(0.02vmin);
  }
  100% {
    transform: rotate(15deg) translate3d(85%, -75%, 0) skew(-30deg) scale(2);
    opacity: 0;
    filter: blur(2.5vmin);
  }
}

@keyframes fade-in {
  0% {
    opacity: 0;
    transform: translate3d(-2vmin, 2vmin, 0);
    filter: blur(1vmin);
  }
  100% {
    opacity: 1;
    transform: translate3d(0);
    filter: blur(0.02vmin);
  }
}
</style>

