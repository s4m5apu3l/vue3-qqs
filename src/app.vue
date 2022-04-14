<template>
  <div class="app">
    <post-form
      @create="createPost"
    />
    <post-list :posts="posts"

    />
  </div>
</template>

<script>
import PostForm from "@/components/PostForm.vue"
import PostList from "@/components/PostList.vue"

  export default {
    components: {
      PostList, PostForm
    },
    data() {
      return {
        posts: [
          {id: 1, title: 'JS', body: 'opisanie'},
          {id: 2, title: 'JS 2', body: 'opisanie 2'},
          {id: 3, title: 'JS 3', body: 'opisanie 3'},
          {id: 4, title: 'JS 4', body: 'opisanie 4'},
        ],
      }
    },
    methods: {
      createPost(post) {
        this.posts.push(post);
      },
    }
  }
</script>

<style>
  .app {
    padding: 20px;
  }

  </style>