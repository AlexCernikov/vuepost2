<template>
<div class="container">
  <post-form @create = "createPost"/>
  <post-list :posts="posts"/> 
  <!-- v-bind:posts -->
</div>
</template>

<script>
import PostForm from '@/components/PostForm';
import PostList from '@/components/PostList';

export default {
  components: {
    PostForm, PostList
    },
  data () {
    return {
     posts: [
       {id:1, title: 'JavaScript 1', body: 'Description 1'},
       {id:2, title: 'JavaScript 2', body: 'Description 2'},
       {id:3, title: 'JavaScript 3', body: 'Description 3'}
     ],
    }
  },
  methods:{
    createPost(post){
      this.posts.push(post)
      
    }
   }
  }
</script>

<style>
*{
padding: 0;
margin: 0;
box-sizing: border-box;
}

.container{
  max-width: 1120px;
  margin: auto;
  }

 
</style>
