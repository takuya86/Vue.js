<template>
  <div>
    <slot name = "title" :user = "user" text="text">
      <!-- <h2>デフォルトのタイトル</h2> --> <!-- フォールバックコンテンツ -->
    </slot>

    <slot></slot>

    <hr>
    <p>いいねの数</p>
    <slot name = "number"></slot>
  </div>
</template>

<script>
export default {
  data() {
    return {
      user: {
        firstName: "Jack",
        lastName: "Donald",
      }
    };
  }
};
</script>

<style>
  h1{
      color: red;
    }
</style>