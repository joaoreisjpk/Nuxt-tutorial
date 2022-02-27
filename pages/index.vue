<template>
  <div>
    <Nav />
    <div class="container">
      <Hero />
      <LargeCardDisplay
        v-for="cardInfo in largeCardInfo"
        :key="cardInfo.id"
        :cardsSection="cardInfo"
      />
      <SmallCardDisplay
        v-for="cardInfo in smallCardInfo"
        :key="cardInfo.id"
        :cardsSection="cardInfo"
      />
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import { largeCardSections, smallCardSections } from "../assets/data";

export default Vue.extend({
  name: "IndexPage",
  data() {
    return {
      largeCardInfo: largeCardSections,
      smallCardInfo: smallCardSections,
    };
  },
});
</script>
