<template>
  <form @submit.prevent>
    <h4>Создание поста</h4>
    <input
        :value="post.title"
        @input="post.title = $event.target.value"
        class="input"
        type="text"
        placeholder="Название"
    />
    <input
        :value="post.body"
        @input="post.body = $event.target.value"
        class="input"
        type="text"
        placeholder="Описание"
    />
    <button
        class="btn"
        @click="createPost">
      Создать
    </button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      post: {
        title: '',
        body: ''
      }
    }
  }
}
</script>

<style scoped>
.input {
  width: 100%;
  border: 1px solid teal;
  padding: 10px 15px;
  margin-top: 15px;
}

.btn {
  margin-top: 15px;
  align-self: flex-end;
  padding: 10px 15px;
  background: none;
  color: teal;
  border: 1px solid teal;
  cursor: pointer;
}

.btn:hover {
  background: teal;
  color: #fff
}

.btn:active {
  opacity: 0.5;
}
</style>