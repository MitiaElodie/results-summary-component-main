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
          icon: "../assets/images/icon-reaction.svg",
          backgroundColor: 'hsla(0, 100%, 67%, 0.1)',
          color: 'hsl(0, 100%, 67%)',
        },
        {
          "category": "Memory",
          value: 92,
          icon: "../assets/images/icon-memory.svg",
          backgroundColor: 'hsla(39, 100%, 56%, 0.1)',
          color: 'hsl(39, 100%, 56%)',
        },
        {
          "category": "Verbal",
          value: 61,
          icon: "../assets/images/icon-verbal.svg",
          backgroundColor: 'hsla(166, 100%, 37%, 0.1)',
          color: 'hsl(166, 100%, 37%)',
        },
        {
          "category": "Visual",
          value: 72,
          icon: "../assets/images/icon-visual.svg",
          backgroundColor: 'hsla(234, 85%, 45%, 0.1)',
          color: 'hsl(234, 85%, 45%)',
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
$light-red: hsl(0, 100%, 67%);
$orange-yellow: hsl(39, 100%, 56%);
$Green-teal: hsl(166, 100%, 37%);
$Cobalt-blue: hsl(234, 85%, 45%);
$Light-slate-blue: hsl(252, 100%, 67%);
$Light-royal-blue: hsl(241, 81%, 54%);
$Violet-blue: hsla(256, 72%, 46%, 1);
$Persian-blue: hsla(241, 72%, 46%, 0);
$white: hsl(0, 0%, 100%);
$Pale-blue: hsl(221, 100%, 96%);
$Light-lavender: hsl(241, 100%, 89%);
$dark-gray-blue: hsl(224, 30%, 27%);

* {
  padding: 0;
  margin: 0;
  font-family: 'Hanken Grotesk', sans-serif;
}
.result {
  &__container {
    min-height: 100vh;
    width: 100vw;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  &__summary-label {
    margin-bottom: 20px;
  }

  &__score {
    margin-bottom: 15px;
  }

  &__continue-button {
    background-color: $dark-gray-blue;
    color: $white;
    padding: 15px;
    border-radius: 30px;
    width: 100%;
    margin-top: 10px;
    font-size: 1em;
  }

  &__summary-label {
    color: $dark-gray-blue;
  }

  &__summary-container {
    max-width: 300px;
  }
}
</style>
