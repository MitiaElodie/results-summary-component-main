<script>
export default {
   name: 'Score',
   props: {
      score: {
         type: Object,
         required: true,
      }
   }
}
</script>

<template>
   <div class="score__container" :style="{ '--background-color': score.backgroundColor, '--color': score.color }">
      <div class="score__category-container">
         <img
            class="score__image"
            :src="score.icon"
         />
         <div class="score__category">{{ score.category }}</div>
      </div>
      <div class="score__value-container">
         <span class="score__value">{{ score.value }}</span>
         <span class="score__of-hundred">
            / 100
         </span>
      </div>
   </div>
</template>

<style lang="scss">
.score {
   &__container {
      display: flex;
      align-items: center;
      justify-content: space-between;
      border-radius: 10px;
      padding: 15px;
      background-color: var(--background-color);
   }

   &__category-container {
      display: flex;
      gap: 10px;
   }

   &__category {
      color: var(--color);
   }

   &__value {
      color: hsl(224, 30%, 27%);
      font-weight: 700;
   }
}
</style>