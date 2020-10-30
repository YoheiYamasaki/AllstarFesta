<template>
    <body>
        <h1 style="color: white;"> オールスター感謝祭 </h1>
        <div class="answer_all">
            <div v-for="(AnswerItem, index) in AnswerItemList" v-bind:key="AnswerItem.rank" v-bind:class="'answer-' + index">
                <Answer :rank="AnswerItem.rank" :name="AnswerItem.name" :seconds="AnswerItem.seconds"/>
            </div>
        </div>
    </body>
</template>

<script>

import Answer from './Answer.vue'
export default {
  name: 'Answers',
  props: {
    msg: String
  },
  components:{
    Answer
  },
  data: function(){
    return {
      AnswerItemList: [
        {rank: 1, name: "Yohei", seconds:1.84},
        {rank: 2, name: "Yohei", seconds:1.84},
        {rank: 3, name: "Yohei", seconds:1.84},
        {rank: 4, name: "Yohei", seconds:1.84},
        {rank: 5, name: "Yohei", seconds:1.84},
        {rank: 6, name: "Yohei", seconds:1.84},
        {rank: 7, name: "Yohei", seconds:1.84},
        {rank: 8, name: "Yohei", seconds:1.84},
        {rank: 9, name: "Yohei", seconds:1.84},
        {rank: 10, name: "Yohei", seconds:1.84},
      ]
    }
  }
}
</script>

<style lang="scss">

.answer_all{
    width: 50%;
    margin: auto;
}

@for $i from 0 through 10 {
    .answer-#{$i}{
        opacity: 0;
        animation-name: AppearAnswer;
        animation-duration: 0.5s;
        animation-delay: calc(0.2s *  (10 - #{$i}));
        animation-fill-mode: forwards; //終了後のスタイルをそのまま使う
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