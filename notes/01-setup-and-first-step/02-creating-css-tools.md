## CSS animation

[MDN - Animation](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/animation-timing-function)

```css
.heading-primary-main {
  display: block;

  font-size: 4rem;
  font-weight: 700;
  letter-spacing: 2rem;

  animation-name: moveInLeft;
  animation-duration: 1s;
  animation-timing-function: ease-out;

  /*
  animation-iteration-count: 3;
  animation-delay: 3s; */
}

.heading-primary-sub {
  display: block;

  font-size: 1.4rem;
  font-weight: 700;
  letter-spacing: 1rem;

  animation-name: moveInRight;
  animation-duration: 1s;
  animation-timing-function: ease-out;
}

@keyframes moveInLeft {
  0% {
    opacity: 0;
    transform: translateX(-100px);
  }

  80% {
    transform: translateX(10px);
  }

  100% {
    opacity: 1;
    transform: translate(0);
  }
}

@keyframes moveInRight {
  0% {
    opacity: 0;
    transform: translateX(100px);
  }

  80% {
    transform: translateX(-10px);
  }

  100% {
    opacity: 1;
    transform: translate(0);
  }
}
```
