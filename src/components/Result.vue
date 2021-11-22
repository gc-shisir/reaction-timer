<template>
  <p>The Score is: {{ score }}ms</p>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
  props: ["score"],
  data() {
    return {
      rank: null,
    };
  },
  mounted() {
    if (this.score <= 250) {
      this.rank = "Fast Response";
    } else if (this.score > 250 && this.score <= 600) {
      this.rank = "Rapid reflexes";
    } else {
      this.rank = "Snail pace";
    }
  },
};
</script>

<style>
.rank {
  font-size: 1.4rem;
  color: teal;
  font-weight: 700;
}
</style>
