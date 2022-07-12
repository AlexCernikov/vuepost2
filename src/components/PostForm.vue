<template>
  <form @submit.prevent>
    <input 
    class="input" 
    
    v-model = "post.title"
    type="text" 
    placeholder="title">

    <input 
    class="input" 
    
    v-model = "post.body"
    type="text" 
    placeholder="description">

    <button 
    class="btn" 
    @click="createPost"
    >Create
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
        this.post.id = Date.now()
        this.$emit('create', this.post)
        this.post = {
          title: '',
          body: ''
       }
   }
   } 
  }
</script>

<style  scoped>
 form{
display: flex;
flex-direction: column;
    }
  .input{
width: 100%;
margin-top: 15px;
border: 1px solid teal;
padding: 10px 15px;
    }

    .btn{
align-self: flex-end;
margin-top: 15px;
padding: 10px 15px;
background: none;
color:teal;
border: 1px solid teal;
      }

</style>