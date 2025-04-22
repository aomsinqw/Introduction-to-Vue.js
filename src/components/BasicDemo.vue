<template>
  <div class="basic-demo">
    <h2>🎓 Vue Template Syntax & Directives</h2>

    <!-- Interpolation -->
    <p>1. Interpolation: จ๊ะเอ๋, {{ name }}!</p>

    <!-- v-text -->
    <p>2. v-text: <span v-text="message"></span></p>

    <!-- v-html -->
    <p>3. v-html: <span v-html="htmlMessage"></span></p>

    <!-- v-show -->
    <p v-show="isVisible">4. v-show: This is visible!</p>

    <!-- v-if / v-else-if / v-else -->
    <div>
      <p v-if="status === 'success'">✅ Success</p>
      <p v-else-if="status === 'error'">❌ Error</p>
      <p v-else> Waiting...</p>
    </div>

    <!-- v-bind -->
    <img :src="imageUrl" :alt="imageAlt" :style="{ width: imgSize + 'px' }" />

    <!-- v-on -->
    <button @click="count++">Click Click: {{ count }}</button>

    <!-- v-model example -->
    <input v-model="name" placeholder="Enter your name" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'ชอบกดไลค์ ใช่กดแชร์ ถ้าบ่มีคนแคร์ ทำไงดี',
      message: 'This text uses v-text!',
      htmlMessage: '<strong style="color:pink">This uses v-html!</strong>',
      isVisible: true,
      status: 'waiting',
      count: 0
    }
  }
}
</script>

<style scoped>
.basic-demo {
  border: 2px dashed #ccc;
  padding: 20px;
  margin-top: 2rem;
}
</style>
