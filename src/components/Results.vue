<template>
  <div>Reaction time: {{ score }} ms</div>
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
    if (this.score < 250) {
      this.rank = " Superfast reflexes";
    } else if (this.score < 400) {
      this.rank = "Fast Fingers";
    } else {
      this.rank = "Snail pace...";
    }
  },
};
</script>

<style>

.rank {
    font-size: 1.4em;
    color: #0faf87;
    font-weight: bold;
}
</style>
