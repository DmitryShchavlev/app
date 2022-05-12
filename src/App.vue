<template>
<div>
   <todo-list />
   <post-form
    @create="createPost"
    />
   <post-list
   :posts="posts"
  
    />

</div>
</template>

<script>
import TodoList from './components/TodoList.vue'

import PostList from '@/components/PostList.vue'
import PostForm from '@/components/PostForm.vue'

export default {
  name: 'App',
  components: {
    TodoList,

    PostList,
    PostForm,
},

 data(){
    return{
      posts: [
        {id: 1, title: 'JavaScript 1', body: 'Описание поста 1' },
        {id: 2, title: 'JavaScript 2', body: 'Описание поста 2' },
        {id: 3, title: 'JavaScript 3', body: 'Описание поста 3' },
        {id: 4, title: 'JavaScript 4', body: 'Описание поста 4' },
        
      ]
    }
  },
  methods:{
    createPost(post){
      this.posts.push(post);
    }
  }
}


</script>

<style>


#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
 /*text-align: center;*/
  color: #2c3e50;
  /*margin-top: 60px;*/
}


</style>
