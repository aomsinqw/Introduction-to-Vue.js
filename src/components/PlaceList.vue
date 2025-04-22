<!-- src/components/PlaceList.vue -->
<template>
  <section>
    <h2>📍 สถานที่ท่องเที่ยวแนะนำในญี่ปุ่น</h2>
    <ul>
      <li
        v-for="(place, index) in places"
        :key="place.id"
        :class="{ highlight: index === selected }"
        :style="{ fontSize: index === selected ? '1.2rem' : '1rem' }"
        @click="selected = index"
      >
        🗾 {{ place.name }} - {{ place.region }}
        <p v-if="index === selected">📌 {{ place.description }}</p>
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  data() {
    return {
      selected: null,
      places: [
        { id: 1, name: 'Mount Fuji', region: 'Chubu', description: 'ภูเขาที่สูงที่สุดในญี่ปุ่น' },
        { id: 2, name: 'Tokyo Tower', region: 'Kanto', description: 'หอคอยสีแดงอันเป็นสัญลักษณ์ของโตเกียว' },
        { id: 3, name: 'Kyoto', region: 'Kansai', description: 'เมืองแห่งวัดและวัฒนธรรมดั้งเดิม' }
      ]
    }
  }
}
</script>

<style scoped>
ul {
  list-style: none;
  padding: 0;
}

li {
  margin: 10px 0;
  cursor: pointer;
  transition: 0.3s ease;
}

.highlight {
  background-color: #fdf0f5;
  font-weight: bold;
}
</style>
