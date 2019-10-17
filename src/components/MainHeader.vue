<template>
  <div class="container">
    <h1>
      we make
      <span class="typed-text">{{ textValue }}</span>
    </h1>
  </div>
</template>

<script>
import { setTimeout } from "timers";
export default {
  name: "MainHeader",
  data() {
    return {
      typingSpeed: 200,
      erasingSpeed: 100,
      newTextDelay: 2000,
      textArray: ["apps", "solutions", "real-life solutions"],
      textValue: "",
      arrayIndex: 0,
      charIndex: 0
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
