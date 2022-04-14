<template>
  <button class="btn">
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: 'my-button'
}
</script>

<style>
  .btn {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 200px;
    height: 4 0px;
    border-radius: 20px;
    padding: 10px 15px;
    background: none;
    color: teal;
    font-size: 20px;
    border: 1px solid teal;
  }
</style>