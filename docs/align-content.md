# align-content

?> align-content 属性定义了多根轴线的对齐方式。如果项目只有一根轴线，该属性不起作用。
<vuep template="#flex-align-content"></vuep>

<script v-pre type="text/x-template" id="flex-align-content">
<template>
  <ul>
    <li>1</li>
    <li>2</li>
    <li>3</li>
    <li>4</li>
    <li>5</li>
  </ul>
</template>
<style>
  ul{
    height: 300px;
    display: flex;
    flex-wrap: wrap;
    color: #fff;
    text-align: center;
  }
  li{
    list-style: none;
    height: 46px;
    margin: 2px;
    width: 30%;
    background: #310736;
  }
  li:nth-child(2){
    height: 96px;
  }
</style>
<script>
</script>
</script>
