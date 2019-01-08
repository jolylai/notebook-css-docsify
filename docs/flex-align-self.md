# align-self

?> `align-self`属性允许单个项目有与其他项目不一样的对齐方式，可覆盖`align-items`属性。默认值为`auto`，表示继承父元素的`align-items`属性，如果没有父元素，则等同于`stretch`。

```css
.box {
  align-items: flex-start | flex-end | center | baseline | stretch;
}
```

<vuep template="#flex-align-self"></vuep>

<script v-pre type="text/x-template" id="flex-align-self">
<template>
  <main>
    <select v-bind:value='alignSelf' v-on:change="handleSelectChange">
      <option value='align-self-flex-start'>flex-start</option>
      <option value='align-self-flex-end'>flex-end</option>
      <option value='align-self-center'>center</option>
      <option value='align-self-baseline'>baseline</option>
      <option value='align-self-stretch'>stretch</option>
    </select>
    <ul class='align-items' >
      <li>1</li>
      <li class='target' v-bind:id='alignSelf'>Target</li>
      <li>3</li>
      <li>4</li>
      <li>5</li>
    </ul>
  </main>
</template>
<style>
  main{
    width: 100%;
  }
  ul{
    height: 300px;
    color: #fff;
    text-align: center;
  }
  li{
    list-style: none;
    height: 46px;
    margin: 2px;
    width: calc(20% - 4px);
    background: #310736;
    border-radius: 4px;

    display: flex;
    align-items: center;
    justify-content: center;
  }
  li:nth-child(2){
    background: #05ffb0;
  }
  li:nth-child(4){
    height: 76px;
  }
  .align-items{
    display: flex;
    flex-wrap: wrap;
    align-items: center;
  }
  #align-self-flex-start{
    align-self: flex-start;
  }
  #align-self-flex-end{
    align-self: flex-end;
  }
  #align-self-center{
    align-self: center;
  }
  #align-self-baseline{
    align-self: baseline;
  }
  #align-self-stretch{
    align-self: stretch;
    height: auto;
  }
</style>
<script>
module.exports = {
  methods:{
    handleSelectChange: function (event) {
      this.alignSelf = event.target.value
    }
  },
  data: () => ({
    alignSelf: 'align-self-center'
  })
}
</script>
</script>

## tip

- `align-items: stretch` 时如果项目未设置高度或设为auto，将占满整个容器的高度。