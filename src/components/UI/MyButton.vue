<template>
  <button class="btn">
    <slot></slot>
  </button>
</template>

<script>
export default {

}
</script>

<style scoped>
.btn {
  padding: 10px 15px;
  margin-top: 15px;
  align-self: flex-end;
  background: none;
  color: teal;
  border: 1px solid teal;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.btn:hover {
  background-color: teal;
  color: #fff;
}

.btn:active {
  opacity: 0.5;
}
</style>