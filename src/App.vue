<script>
import PlaceList from './components/PlaceList.vue'
import BasicDemo from './components/BasicDemo.vue'
import ApiDemo from './components/ApiDemo.vue'

export default {
  components: {
    PlaceList,
    BasicDemo,
    ApiDemo
  }
}
</script>

<template>
  <div id="app">
    <h1>🇯🇵 เที่ยวญี่ปุ่นกัน
     🇯🇵</h1>
    <PlaceList />
    <BasicDemo />
    <ApiDemo />
  </div>
</template>
