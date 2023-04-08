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
   <div class="score__container">
      <div class="score__category-container">
         <img
            class="score__image"
            :src="score.icon"
         />
         <div class="score__title">{{ score.category }}</div>
      </div>
      <div class="score__value-container">
         <span class="score__value">{{ score.value }}</span>
         <span class="score__of-hundred">
            / 100
         </span>
      </div>
   </div>
</template>