<template>
  <div class="post">
    <div>
      <div><strong>nazvanie: </strong>{{ post.title }}</div>
    <div><strong>opisanie: </strong>{{ post.body }}</div>
    </div>
    <div class="post__btns">
      <my-button>Delete</my-button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    post: {
      type: Object,
      required: true,
    }
  }
}
</script>

<style>

</style>