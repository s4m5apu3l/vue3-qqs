<template>
  <div>
    <form @submit.prevent>
      <my-input v-model="post.title"   type="text" placeholder="nazvanuie"/>
      <my-input v-model="post.body"   type="text" placeholder="opisnaie"/>
      <my-button class="btn" @click="createPost">CREATE</my-button>
    </form>
  </div>
</template>

<script>
import MyButton from './UI/MyButton.vue';
import MyInput from './UI/MyInput.vue';
export default {
  components: { MyButton, MyInput },
  data() {
    return {
      post: {
        title: '',
        body: '',
      }
    }
  },
  methods: {
    createPost() {
      this.post.id = Date.now();
      this.$emit('create', this.post)
      this.post = {
        title: "",
        body: "",
      }
    }
  }
}
</script>

<style>

</style>