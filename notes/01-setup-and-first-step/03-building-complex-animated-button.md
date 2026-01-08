## Building complex animated button

```css
@keyframes btnMoveInBottom {
  0% {
    opacity: 0;
    transform: translateY(50px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

.btn:link,
.btn:visited {
  text-transform: uppercase;
  text-decoration: none;

  padding: 15px 40px;
  display: inline-block;
  border-radius: 200px;

  position: relative;

  transition: all 0.3s ease-out;
}

.btn:hover {
  transform: translateY(-3px);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
}

.btn:active {
  transform: translateY(-1px);
  box-shadow: 0 5px 6px rgba(0, 0, 0, 0.2);
}

.btn-white {
  background-color: #fff;
  color: #777;
}

.btn-animated {
  animation: btnMoveInBottom 1s ease-out 0.75s;
  animation-fill-mode: backwards;
}

.btn::after {
  content: "";
  display: inline-block;
  height: 100%;
  width: 100%;
  border-radius: 200px;

  position: absolute;
  top: 0;
  left: 0;

  z-index: -1;

  transition: all 0.4s ease-out;
}

.btn-white::after {
  background-color: #fff;
}

.btn:hover::after {
  transform: scaleX(1.1) scaleY(1.2);
  opacity: 0;
}
```

[Next: Section 3 - How CSS works](../02-how-css-works)
