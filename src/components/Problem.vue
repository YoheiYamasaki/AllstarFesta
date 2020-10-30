<template>
  <div class="problem">

  </div>
</template>

<script>
export default {
  name: "Problem",
  props:{
      type: String,
      txt: String,
      img_path: String,
  }
}
</script>

<style>

.problem{
    background-color: aquamarine;
    border: solid;
    border-radius: 0.5em;
    width: 50%;
    height: 100px;
}

</style>