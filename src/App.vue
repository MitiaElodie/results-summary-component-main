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
        <button class="result__continue-button">Continue</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
}
</script>

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
