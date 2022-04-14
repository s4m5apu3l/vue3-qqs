<template>
  <div>
    <h3>Users item</h3>
    <post-item 
    v-for="post in posts"
    :post="post"
    />
  </div>
</template>

<script>
import PostItem from '@/components/PostItem.vue'
export default {
  components: { PostItem },
  props: {
    posts: {
      type: Array,
      requiredL: true,
    }
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
    display: flex;
    align-items: center;
    justify-content: flex-start;
  }
</style>