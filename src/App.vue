<template>
  <div class="app">
    <post-form :title="title" :body="body"/>
    <post-list :posts="posts"/>
  </div>
</template>

<script>
import PostList from "@/components/PostList"
import PostForm from "@/components/PostForm";

export default {
  components: {
    PostList, PostForm
  },
  data() {
    return {
      posts: [
        { id: 1, title: 'JavaScript', body: 'Описание поста' },
        { id: 2, title: 'JavaScript 2', body: 'Описание поста 2' },
        { id: 2, title: 'JavaScript 3', body: 'Описание поста 3' },
      ],
      title: '',
      body: '',
    }
  },
  methods: {
    createPost() {
      const newPost = {
        id: new Date(),
        title: this.title,
        body: this.body
      }
      this.posts.push(newPost)
      this.title = ''
      this.body = ''
    },
  }
}

</script>

<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

.app {
  padding: 20px;
}

form {
  display: flex;
  flex-direction: column;
}

</style>