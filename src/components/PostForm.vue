<template>
    <div>
      <div class="addPost">
        <form @submit.prevent="createPost">
          <h4>Добавить пост</h4>
          <input 
          v-model="post.title"
          type="text" 
          placeholder="Пост">
          <input 
          v-model="post.body"
          type="text"
          placeholder="Описание">
          <button>Добавить</button>
        </form>
      </div>
    </div>
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
            this.post.id = Date.now()
            this.$emit('create', { ...this.post })
            this.post = {
                title: '',
                body: ''
            }
        }
    }
   }
</script>

<style>
.post, .addPost {
  border: 1px solid #ccc;
  padding: 10px;
  margin: 10px;
} 
</style>
