<template>
  <div id="app">
    <header>
      <h1>Explore the Best of Japan: A Journey Like No Other!</h1>
    </header>
    <main>
      <section v-for="place in places" :key="place.id" class="place">
        <h2>{{ place.name }}</h2>
        <img :src="place.image" :alt="place.name" class="place-image" />
        <p>{{ place.description }}</p>
        <a :href="place.link" target="_blank">ดูรายละเอียดเพิ่มเติม</a>
      </section>
    </main>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      places: [
        {
          id: 1,
          name: "ฟูจิซัง (Mount Fuji)",
          image: "https://kiji.life/newkiji/wp-content/uploads/2022/09/kiji-best-views-of-mt-fuji-10--yamanashi-4.jpg", // เปลี่ยนเป็น URL ของภาพจริง
          description: "ฟูจิซังเป็นภูเขาที่สูงที่สุดในญี่ปุ่นและเป็นสัญลักษณ์ที่สำคัญ",
          link: "https://www.japan.travel/en/uk/inspiration/mount-fuji/"
        },
        {
          id: 2,
          name: "โตเกียวทาวเวอร์ (Tokyo Tower)",
          image: "https://www.govivigo.com/content/ideas/5633/56339a3bec60adb92a8b45c3-2-full-ideas.jpg", // เปลี่ยนเป็น URL ของภาพจริง
          description: "โตเกียวทาวเวอร์เป็นหอคอยที่สูงและมีความสำคัญทางประวัติศาสตร์",
          link: "https://www.tokyotower.co.jp/en.html"
        },
        {
          id: 3,
          name: "เกียวโต (Kyoto)",
          image: "https://content.fun-japan.jp/renewal-prod/cms/articles/content/Kyotojpg_2020-02-20-03-14-01.jpg", // เปลี่ยนเป็น URL ของภาพจริง
          description: "เกียวโตเป็นเมืองที่เต็มไปด้วยวัดและสวนญี่ปุ่นที่สวยงาม",
          link: "https://www.japan.travel/en/uk/regions/kinki/kyoto/"
        }
      ]
    }
  }
}
</script>

<style scoped>
#app {
  font-family: Arial, sans-serif;
  text-align: center;
  padding: 20px;
}

header {
  background-color: #FFF0F5;
  padding: 20px;
}

h1 {
  color: #333;
}

.place {
  margin-bottom: 30px;
}

.place h2 {
  font-size: 1.5rem;
  color: #2c3e50;
}

.place-image {
  width: 100%;
  height: auto;
  max-width: 600px;
  margin-top: 10px;
}

a {
  display: inline-block;
  margin-top: 10px;
  color: #FF3366 ;
  text-decoration: none;
}

a:hover {
  text-decoration: underline;
}
</style>
