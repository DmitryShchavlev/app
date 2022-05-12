<template>
  <div>
      <h3>Список пользователей</h3>
      <post-item
       v-for="post in posts" v-bind:key="post"
       :post="posts"
       />
  </div>
</template>

<script>

import PostItem from "@/components/PostIem";

export default {
    components: {PostItem},

    props:{
        post:{
            type: Object,
            required: true,
        }
    }

}
</script>

<style>
.post{
  padding: 15px ;
  border: 2px solid teal ;
  margin-top: 15px; 
  display:flex ;
  align-items: center;
  justify-content: space-between;
}

</style>