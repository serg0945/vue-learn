<template>
    <div>
      <div class="post" v-for="post in posts" :key="post.id">
        <p>Пост о Vue.js: {{ post.title }}</p>
        <p>Описание Vue.js: {{ post.body }}</p>
      </div>
    </div>
</template>

<script>
 export default {
        props: {
            posts: {
                type: Array,
                required: true
            }
        }    
    }
</script>

<style>
.post {
  border: 1px solid #ccc;
  padding: 10px;
  margin: 10px;
} 
</style>
