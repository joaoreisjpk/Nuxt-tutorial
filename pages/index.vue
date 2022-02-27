<template>
  <div>
    <Hero />
    <LargeCardDisplay
      v-for="cardInfo in largeCardInfo"
      :key="cardInfo.id"
      :cardsSection="cardInfo"
    />
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import { largeCardSections } from "../store/data";

export default Vue.extend({
  name: "IndexPage",
  data() {
    return {
      largeCardInfo: largeCardSections,
    };
  },
});
</script>
