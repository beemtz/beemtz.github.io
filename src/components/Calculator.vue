<template>
  <div class="container">
    <div class="field">
      <label class="label">Number of Questions</label>
      <div class="control">
        <input class="input" type="number" v-model="questionCount" @input="adjustAnswers('wrong')">
      </div>
    </div>
    <div class="field">
      <label class="label">Wrong Answers</label>
      <div class="control">
        <input class="input" type="number" v-model="wrongAnswers" @input="adjustAnswers('wrong')">
      </div>
    </div>
    <div class="field">
      <label class="label">Right Answers</label>
      <div class="control">
        <input class="input" type="number" v-model="rightAnswers" @input="adjustAnswers('right')">
      </div>
    </div>
    <div class="grade">
      {{ finalGrade }}
    </div>
  </div>
</template>

<script>
export default {
  name: 'calculator',
  data () {
    return {
      questionCount: 10,
      wrongAnswers: 0,
      rightAnswers: 10
    }
  },
  methods: {
    adjustAnswers (answers) {
      if (answers === 'right') {
        this.wrongAnswers = this.questionCount - this.rightAnswers
      } else {
        this.rightAnswers = this.questionCount - this.wrongAnswers
      }
    }
  },
  computed: {
    finalGrade () {
      return parseInt((this.rightAnswers / this.questionCount) * 100).toString() + '%'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/styles/vars";

.container {
  background-color: $paper;
}

.label {
  color: $ballpoint;
}

.grade {
  font-family: $marks;
  font-size: 3rem;
  color: $grade;
}
</style>