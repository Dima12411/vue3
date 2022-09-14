<template>
  <div class="main">
    <h1 class="title">Welcome</h1>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.main {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.title {
  font-size: 40px;
}

.rout {
  text-decoration: none;
  color: teal;
  font-size: 20px;
}

.rout:hover {
  opacity: 0.5;
}

.rout:active {
  color: black;
}
</style>