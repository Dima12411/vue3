<template>
  <form @submit.prevent>
    <h4>Создание поста</h4>
    <input
        v-model="post.title"
        class="input"
        type="text"
        placeholder="Название"
    />
    <input
        v-model="post.body"
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
  },
  methods: {
    createPost() {
      this.post.id = new Date()
      this.$emit('create', this.post)
      this.posts = {
        title: '',
        body: '',
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