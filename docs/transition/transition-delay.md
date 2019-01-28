# transition-delay

?> 定义背景如何在元素内延伸

```css
.box {
  background-clip: border-box | padding-box | content-box; /* default border-box */
}
```

<vuep template="#flex--grow"></vuep>

<script v-pre type="text/x-template" id="flex--grow">
<template>
  <ul>
    <li class='transition'><p class='square square-alpha'>Hover me</p></li>
    <li class='transition transition-delay-12s'><p class='square square-alpha'>Hover me</p></li>
    <li class='transition transition-delay-2400ms'><p class='square square-alpha'>Hover me</p></li>
    <li class='transition transition-delay--500ms'><p class='square square-alpha'>Hover me</p></li>
  </ul>
</template>
<style>
ul{
  list-style: none;
}

li{
  margin: 8px 0;
  box-shadow: 2px 2px 1px #eee;
}

p{
  margin: 0;
}

.square{
  width: 75px;
  height: 75px;
  border-radius: 4px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.square-alpha{
  background: #05ffb0;
  color: #310736;
}

.transition>.square{
  transition-property: all;
  transition-duration: 1s;
  transition-timing-function: linear;
  transition-delay: 0s;
}

.transition:hover>.square{
  background: red;
  transform: translateX(160px)
}

.transition-delay-12s .square{
  transition-delay: 1.2s
}

.transition-delay-2400ms .square{
  transition-delay: 2400ms;
}

.transition-delay--500ms .square{
  transition-delay: -500ms;
}

</style>
<script>
</script>
</script>
