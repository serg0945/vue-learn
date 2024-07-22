<template>
  <div>
    <post-form @create="createPost" />
    <post-list :posts="posts" />
  </div>
</template>

<script>
import PostForm from '@/components/PostForm'
import PostList from '@/components/PostList'

export default {
  components: { PostForm, PostList },
  data() {
    return {
      posts: [
        { id: 1, title: 'Пост 1', body: 'Описание поста 1' },
        { id: 2, title: 'Пост 2', body: 'Описание поста 2' },
        { id: 3, title: 'Пост 3', body: 'Описание поста 3' },
      ],
    }
  },
  methods: {
    createPost(post) {
      this.posts.push(post);
    }
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
