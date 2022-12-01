<template>
  <div>
    <div class="container">
      <LargeCardDisplay :cardsSection="largeCardInfo[0]" />

      <SmallCardDisplay
        v-for="cardInfo in smallCardSections"
        :key="cardInfo.id"
        :cardSection="cardInfo"
      />
    </div>
  </div>
</template>

<script>
import { smallCardSections, largeCardSections } from "../../assets/data";
export default {
  data() {
    return {
      largeCardInfo: largeCardSections,
      smallCardSections,
    };
  },
};
</script>

<style scoped></style>
