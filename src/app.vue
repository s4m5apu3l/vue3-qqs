<template>
  <div>
    <div>
      <form>
        <input @input="title = $event.target.value" v-bind:value="title" class="input" type="text" placeholder="nazvanuie">
        <input @input="body = $event.target.value" v-bind:value="body" class="input" type="text" placeholder="opisnaie">
        <button @click="createPost">create</button>
      </form>
    </div>
    <div class="post" v-for='(post, index ) in posts' :key="index">
      <div><strong>nazvanie: </strong>{{ post.title }}</div>
      <div><strong>nazvanie: </strong>{{ post.body }}</div>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        posts: [
          {id: 1, title: 'JS', body: 'opisanie'},
          {id: 2, title: 'JS 2', body: 'opisanie 2'},
          {id: 3, title: 'JS 3', body: 'opisanie 3'},
        ],
        title: '',
        body: '',
      }
    },
    methods: {
      createPost() {
        const newPost = {
          id: Date.now(),
          title: this.title,
          body: this.body,
        }
      },
    }
  }
</script>

<style>
 * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  .post {
    border: 1px solid black;
    margin-top: 20px;
  }

  </style>