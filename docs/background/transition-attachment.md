# background-attachment

?> `flex-basis`属性定义了在分配多余空间之前，项目占据的主轴空间（main size）。浏览器根据这个属性，计算主轴是否有多余空间。它的默认值为 auto，即项目的本来大小。

```css
.box {
  background-attachment: scroll | fixed | inherit; /* default scroll */
}
```

<vuep template="#background--attachment"></vuep>

<script v-pre type="text/x-template" id="background--attachment">
<template>
  <main>
    <section></section>
    <section></section>
  </main>
</template>
<style>
  main{
    width: 100%;
  }
  section{
    height: 300px;
  }
  section:first-child{
    margin-bottom: 8px;
    background-image: url('./static/landscape.jpg');
    background-attachment: scroll;
    background-size: cover;
  }
  section:last-child{
    background-image: url('./static/landscape.jpg');
    background-attachment: fixed;
    background-size: cover;
  }
</style>
<script>
</script>
</script>
