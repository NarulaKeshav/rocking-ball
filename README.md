# Rocking Ball
Inspired by [Smile on CodePen](http://codepen.io/rockteam/details/dGvdyx#stats), I wanted to learn how `@keyframes` worked in CSS. So I wanted to give it a shot. 

So I present it to you, my Chucky and Cheeze (They actually rock):

[View Chucky and Cheeze](http://narulakeshav.github.io/rocking-ball/)

![Screenshot](http://goo.gl/UaGU6Z)

# How it Works
`@keyframes` in CSS lets you animate HTML elements. In order to rock the balls, I used `@keyframes` at `45%`, `50%`, `55%` and `90%` by changing transform property. At `50%` and `95%`, I rotated the eyes at `x-axis` in order to make the eyes blink. Something like this:

I gave the class to the div tag that I'm going to target with CSS
```
<div class="left-eye"></div>
<div class="right-eye"></div>
```

Adding properties and animation property to the classes
```
.left-eye, .right-eye {
  background: rgba(0,0,0,0.6);
  height: 45px;
  width: 35px;
  border-radius: 100%;
  position: absolute;
  animation: blink 4s ease-in-out infinite;
}
```

Creating the blink animation at frames
```
@-webkit-keyframes blink {
  45% { -webkit-transform: none; }
  50% { -webkit-transform: rotateX(90deg); }
  55% { -webkit-transform: none; }
  90% { -webkit-transform: none; }
  95% { -webkit-transform: rotateX(90deg); }
}
```

# Why?
I say why not? Learning is learning. Doesn't matter if it's programming or animation. If I like it, I do it. 