# transition-delay

?> transition-property transition-duration transition-timing-function 和 transition-delay 的简写。只有 `transition-duration` 必传；

<vuep template="#flex--grow"></vuep>

<script v-pre type="text/x-template" id="flex--grow">
<template>
  <ul>
    <li class='transition transition-1s'><p class='square square-alpha'>Hover me</p></li>
    <li class='transition transition-1s-linear'><p class='square square-alpha'>Hover me</p></li>
    <li class='transition transition-background-1s-linear'><p class='square square-alpha'>Hover me</p></li>
    <li class='transition transition-background-1s-linear-delay'><p class='square square-alpha'>Hover me</p></li>
    <li class='transition transition-background-4s-transform-1s'><p class='square square-alpha'>Hover me</p></li>
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

.transition:hover>.square{
  background: red;
  transform: translateX(160px)
}

.transition-1s>.square{
  transition: 1s;
}

.transition-1s-linear>.square{
  transition: 1s linear;
}
.transition-background-1s-linear>.square{
  transition: background 1s linear;
}
.transition-background-1s-linear-delay>.square{
  transition: background 1s linear 500ms;
}
.transition-background-4s-transform-1s>.square{
  transition: background 4s, transform 1s;
}
</style>
<script>
</script>
</script>

?> transition: 1s;

- transition-duration: 1s
- transition-property: all; default
- transition-timing-function: ease; default
- transition-delay: 0s; default

?> transition: 1s linear;

- transition-duration is set to 1s
- transition-property defaults to all
- transition-timing-function is set to linear
- transition-delay defaults to 0s

?> transition: background 1s linear;

- transition-duration is set to 1s
- transition-property is set to background
- transition-timing-function is set to linear
- transition-delay defaults to 0s

?> transition: background 1s linear 500ms;

- transition-duration is set to 1s
- transition-property is set to background
- transition-timing-function is set to linear
- transition-delay is set to 500ms

?> transition: background 4s, transform 1s;

- You can combine multiple properties with their own transition duration.
