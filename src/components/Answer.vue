<template>
    <div class="answer_row">
      <span class="answer_rank"> {{rank}} </span>
      <span class="answer_name"> {{name}} </span>
      <span class="answer_seconds"> {{seconds}} </span>
    </div>
</template>

<script>
export default {
name: 'Answer',
  props: {
    rank: Number,
    name: String,
    seconds: Number
  }
}
</script>

<style lang="scss">
  .answer_row{
    height: 10%;
    background-color: blue;
    margin: 0.1em 0;

    font-size: 2.5em;
    color: honeydew;
    text-shadow: 0.08em 0.1em black;
    border: 2px solid;
    border-radius: 0.5em;
    border-color:white;

    display: flex;
    justify-content: space-between;

    .answer_rank{
      display: inline-block;
      width: 10%;
      text-align: center;
      border-radius: 0.5em;
      background: linear-gradient(#05FBFF, #1E00FF);
      /* background-color: #05FBFF; */
    }

    .answer_name{
      display: inline-block;
      width: 50%;
    }

    .answer_seconds{
      display: inline-block;
      width: 20%;
    }
}

@keyframes AppearAnswer{
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
</style>