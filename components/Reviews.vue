<template>
  <div>
    <h3>Customer Reviews</h3>
    <div></div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      reviewers: [],
    };
  },
  async fetch() {
    this.reviwers = await fetch("https://randomuser.me/api/?results=5").then(
      (res) => res.json()
    );
  },
};
</script>

<style lang="scss" scoped></style>
