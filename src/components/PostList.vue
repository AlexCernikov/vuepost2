<template>
<div>
  <h3>List of Users</h3>
   <post-item 
   v-for="post in posts" 
   :post="post"/>
</div>

</template>

<script>
import PostItem from '@/components/PostItem'
  export default {
    components: {PostItem},
     props: {
       posts: {
         type: Array,
         required: true
         }
      }
  }
</script>

<style  scoped>
.post{
padding: 15px;
border:3px solid teal;
margin-top: 15px;
  }

</style>