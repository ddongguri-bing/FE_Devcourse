<script>
import { data } from "autoprefixer";

export default {
  name: "First",
  data() {
    return {
      count: 0,
      array: [1, 2, 3],
    };
  },
  // 감시자 속성
  // 특정 데이터에 변화가 있느냐가 중요
  watch: {
    // 깊은 사용법
    array: {
      handler(cur, prev) {
        console.log(`이전 값 : ${prev}`);
        console.log(`현재 값 : ${cur}`);
      },
    },
    // 기본 사용법
    count(cur, prev) {
      console.log(`이전 값 : ${prev}`);
      console.log(`현재 값 : ${cur}`);
    },
  },
  // beforeCreate에서는 어떠한 값에도 접근할 수 없다
  beforeCreate() {
    console.log("beforeCreate", this.count);
  },
  created() {
    console.log("created", this.count);
  },
  beforeMount() {
    console.log("beforeMount");
  },
  mounted() {
    console.log("mounted");
  },
  beforeUpdate() {
    console.log("beforeUpdate", this.count);
  },
  updated() {
    console.log("updated", this.count);
  },
  beforeUnmount() {
    console.log("beforeUnmount");
  },
  unmounted() {
    console.log("unmounted");
  },
};
</script>
<template>
  <div>
    <h1>First Component</h1>

    <p>{{ count }}</p>
    <button @click="count++">증가</button>

    <p>{{ array }}</p>
    <button @click="">수정</button>
  </div>
</template>
<style></style>
