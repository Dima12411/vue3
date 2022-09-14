<template>
  <div class="post">
    <div class="post__wrapper">
      <div>
        <strong>Название:</strong>
        {{ post.title }}
      </div>
      <div>
        <strong>Описание:</strong>
        {{ post.body }}
      </div>
    </div>
    <div class="post__btns">
      <my-button
          @click="$router.push(`posts/${post.id}`)"
          class="button"
      >
        Открыть
      </my-button>
      <my-button
          @click="$emit('remove', post)"
          class="button"
      >
        Удалить
      </my-button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    post: {
      type: Object,
      required: true,
    }
  }
}
</script>

<style scoped>
.post {
  padding: 15px;
  border: 2px solid teal;
  margin-top: 15px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.post__wrapper {
  display: flex;
  flex-direction: column;
}

.post__btns {
  display: flex;
}

.button {
  margin-left: 5px;
}
</style>