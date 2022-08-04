<template>
  <div>
    <button>Like</button>
    <button>Dislike</button>
  </div>
  <div>Number of likes: <strong>{{ likes }}</strong></div>
  <div>Number of dislikes: <strong>{{ dislikes }}</strong></div>
</template>

<script>
export default {
  data() {
    return {
      likes: 5,
      dislikes: 0,
    }
  },
}

</script>

<style>

</style>