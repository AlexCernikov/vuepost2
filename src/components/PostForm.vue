<template>
  <form @submit.prevent>
    <input 
    class="input" 
    v-bind:value="post.title" 
    @input="post.title = $event.target.value"
    type="text" 
    placeholder="title">

    <input 
    class="input" 
    v-bind:value="post.body" 
    @input="post.body = $event.target.value"
    type="text" 
    placeholder="description">

    <button 
    class="btn" 
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