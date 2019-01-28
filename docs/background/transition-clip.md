# background-clip

?> 定义背景如何在元素内延伸

```css
.box {
  background-clip: border-box | padding-box | content-box; /* default border-box */
}
```

<vuep template="#flex--grow"></vuep>

<script v-pre type="text/x-template" id="flex--grow">
<template>
  <main>
    <select v-on:change="handleSelectChange">
      <option value='borderBox'>border-box</option>
      <option value='paddingBox'>padding-box</option>
      <option value='contentBox'>content-box</option>
    </select>
    <section v-bind:class="{ 'background-clip-border-box': borderBox,'background-clip-padding-box': paddingBox, 'background-clip-content-box': contentBox }">
      background-clip
    </section>
  </main>
</template>
<style>
  main {
    width: 100%;
  }
  select {
    margin-bottom: 8px;
  }
  section {
    width: 100%;
    padding: 2em;
    border: 6px dashed;
    background-color: #05ffb0;
    background-clip: content-box;
  }
  .background-clip-border-box{
    background-clip: border-box;
  }
  .background-clip-padding-box{
    background-clip: padding-box;
  }
  .background-clip-content-box{
    background-clip: content-box;
  }
</style>
<script>
module.exports = {
  methods:{
    handleSelectChange: function (event) {
      const value = event.target.value
      if(value==='borderBox'){
        this.borderBox = true
        this.paddingBox = false
        this.contentBox = false
      }
      if(value==='paddingBox'){
        this.borderBox = false
        this.paddingBox = true
        this.contentBox = false
      }
      if(value==='contentBox'){
        this.borderBox = false
        this.paddingBox = false
        this.contentBox = true
      }
    }
  },
  data: () => ({
    borderBox: true,
    paddingBox: false,
    contentBox: false
  })
}
</script>
</script>
