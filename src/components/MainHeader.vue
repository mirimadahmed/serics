<template>
  <div class="container">
    <h1>
      we
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
      typingSpeed: 100,
      erasingSpeed: 100,
      newTextDelay: 2000,
      textArray: ["make apps", "craft solutions", "are SERICS"],
      textValue: "",
      arrayIndex: 0,
      charIndex: 0
    };
  },
  methods: {
    typeText() {
      if (this.charIndex < this.textArray[this.arrayIndex].length) {
        this.textValue += this.textArray[this.arrayIndex].charAt(
          this.charIndex
        );
        this.charIndex += 1;
        setTimeout(this.typeText, this.typingSpeed);
      } else {
        setTimeout(this.eraseText, this.newTextDelay);
      }
    },
    eraseText() {
      if (this.charIndex > 0) {
        this.textValue = this.textArray[this.arrayIndex].substring(
          0,
          this.charIndex - 1
        );
        this.charIndex -= 1;
        setTimeout(this.eraseText, this.erasingSpeed);
      } else {
        this.typeStatus = false;
        this.arrayIndex += 1;
        if (this.arrayIndex >= this.textArray.length) this.arrayIndex = 0;
        setTimeout(this.typeText, this.typingSpeed + 1000);
      }
    }
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
