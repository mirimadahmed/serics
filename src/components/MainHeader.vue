<template>
  <div class="container">
    <h1>
      we make
      <span class="typed-text">apps</span>
    </h1>
  </div>
</template>

<script>
import { setTimeout } from "timers";
export default {
  name: "MainHeader",
  data() {
    return {
      newTextDelay: 2000
    };
  },
  methods: {
    typeText() {},
    eraseText() {}
  },
  created() {
    setTimeout(this.typeText, this.newTextDelay + 200);
  }
};
</script>

<style scoped>
.container {
  width: 100%;
  height: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
}
h1 {
  font-weight: bolder;
  font-size: 6rem;
}
.typed-text {
  color: #e74c3c;
}
</style>
