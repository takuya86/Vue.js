<template>
  <div>
    <LikeHeader>

      <h2>みなさん</h2>

      <template v-slot:title> <!-- 名前付きslot -->
        <h2>こんにちは</h2>
      </template>

      <h3>はじめまして</h3>
      <p>よろしくお願いします</p>

      <template v-slot:number>
        <p>{{ number }}</p>
      </template>
      <!-- <h1>トータルのいいね数</h1>
      <h2>{{ number }}</h2> -->
    </LikeHeader>
    <LikeNumber :total-number="number" v-on:my-click="number = $event"></LikeNumber>
    <LikeNumber :total-number="number" @my-click = "incrementNumber"></LikeNumber>
  </div>
</template>

<script>
import LikeHeader from "./LikeHeader.vue";

export default {
  data() {
    return {
      number: 14
    };
  },
  components: {
    LikeHeader
  },
  methods: {
    incrementNumber (value) {
      this.number = value;
    },
  },
};
</script>

<style scoped>
  div {
    border: 1px solid blue
  }
  h1{
    color: blue;
  }
</style>