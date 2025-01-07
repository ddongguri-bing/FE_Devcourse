<script>
import First from "./components/First.vue";

export default {
  name: "App",
  components: { First },
  data() {
    return {
      isShow: true,
    };
  },
};
</script>
<template>
  <div class="wrapper">
    <h1>LifeCycle : 생명주기</h1>
    <!--
      # 라이프사이클 훅
        라이프사이클마다 라이프사이클 훅 2개가 세트
          - 실행 전 before
          - 실행 후 -ed
    -->
    <First />
    <button>상태 제어</button>
  </div>
</template>
<style>
.wrapper {
  padding: 30px 0;
  border-bottom: 1px solid #828282;
  margin-bottom: 30px;
}
h1 {
  font-size: 30px;
  font-weight: 700;
}
</style>
