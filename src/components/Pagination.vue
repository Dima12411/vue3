<template>
  <div class="page__wrapper">
    <div
        class="page"
        v-for="pageNumber in pages"
        :key="pageNumber"
        :class="{
          'current-page': currentPage === pageNumber
        }"
        @click="$emit('change', pageNumber)"
    >
      {{ pageNumber }}
    </div>
  </div>
</template>

<script>
export default {
  name: 'pagination',
  props: {
    pages: {
      type: Number,
      required: true,
    },
    currentPage: {
      type: Number,
      required: true,
    }
  }
}
</script>

<style scoped>
.page__wrapper {
  display: flex;
  margin-top: 15px;
}

.page {
  border: 1px solid black;
  padding: 20px;
  margin-left: 3px;
  transition: background-color 0.3s ease;
  cursor: pointer;
}

.page:first-child {
  margin: 0;
}

.page:hover {
  background-color: teal;
  color: #fff;
}

.current-page {
  border: 2px solid teal
}
</style>