<!-- src/components/ApiDemo.vue -->
<template>
  <div class="api-demo">
    <h2>🌐 ดึงข้อมูลผู้ใช้งานจาก API</h2>

    <button @click="fetchUsers">โหลดข้อมูล</button>

    <ul v-if="users.length">
      <li v-for="user in users" :key="user.id">
        👤 {{ user.name }} ({{ user.email }})
      </li>
    </ul>

    <p v-else>⏳ ยังไม่มีข้อมูล</p>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  data() {
    return {
      users: []
    }
  },
  methods: {
    async fetchUsers() {
      try {
        const res = await axios.get('https://jsonplaceholder.typicode.com/users')
        this.users = res.data
      } catch (err) {
        console.error('เกิดข้อผิดพลาดในการโหลดข้อมูล:', err)
      }
    }
  }
}
</script>

<style scoped>
.api-demo {
  border: 2px solid #ddd;
  padding: 20px;
  margin-top: 2rem;
  background-color: #f7f7f7;
}
button {
  padding: 10px 15px;
  background-color: #42b983;
  border: none;
  color: white;
  cursor: pointer;
  margin-bottom: 1rem;
}
button:hover {
  background-color: #369e6f;
}
</style>