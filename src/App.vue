<script>
import Score from '@/components/Score.vue'
export default {
  name: 'App',

  components: { Score },

  data() {
    return {
      scoreList: [
        {
          category: "Reaction",
          value: 80,
          icon: "@/assets/images/icon-reaction.svg"
        },
        {
          "category": "Memory",
          value: 92,
          icon: "@/assets/images/icon-memory.svg"
        },
        {
          "category": "Verbal",
          value: 61,
          icon: "@/assets/images/icon-verbal.svg"
        },
        {
          "category": "Visual",
          value: 72,
          icon: "@/assets/images/icon-visual.svg"
        }
      ]
    }
  }
}
</script>

<template>
  <div id="app" class="result__container">
    <div class="result__content">
      <div class="result__overview-container">
        <p class="result__your-result-label">You result</p>
        <div class="result__score-container">
          <div class="result__global-score">76</div>
          <div class="result__of-hundred">of 100</div>
        </div>
        <p class="result__comment">Great</p>
        <p class="result__description">
          You scored higher than 65% of the people who have taken these tests.
        </p>
      </div>
      <div class="result__summary-container">
        <h3 class="result__summary-label">Summary</h3>
        <div class="result__score-list">
          <Score
            v-for="(score, index) in scoreList"
            :key="index"
            class="result__score"
            :score="score"
          />
        </div>
        <button class="result__continue-button">Continue</button>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
* {
  padding: 0;
  margin: 0;
}
.result {
  &__container {
    min-height: 100vh;
    width: 100vw;
    display: flex;
    align-items: center;
    justify-content: center;
  }
}
</style>
