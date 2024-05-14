<template>
  <div>

    <h1 :class="{ 'title': true, 'title-home': isHome }">Curso Vue3</h1>

    <p :class="pClass">
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusamus eum itaque explicabo qui nemo perferendis expedita saepe quaerat ipsam consectetur nostrum officia ipsum placeat, natus corrupti voluptatem cum fugit voluptatum!
    </p>

    <p :style="styleClass">
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusamus eum itaque explicabo qui nemo perferendis expedita saepe quaerat ipsam consectetur nostrum officia ipsum placeat, natus corrupti voluptatem cum fugit voluptatum!
    </p>

    <div 
        v-for="(obj, index) in todos" 
        :key="obj.id"
        class="todos-item"
      >
        <img 
          v-if="obj.imgSrc"
          :src="obj.imgSrc" 
          alt=""
        >
        {{ index }} - {{ obj.title }}
    </div>

  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
// import TheHeader from './components/TheHeader.vue'

export default {
  name: 'App',
    data() {
      return {
        isHome: true,
        classVar: 'title',
        pClass: ['text', 'text-home'],
        styleClass: { color: 'aqua', backgroundColor: 'black', 'font-size': '20px' },
        todos: [
          {
              "userId": 1,
              "id": 1,
              "title": "delectus aut autem",
              "completed": false,
              "imgSrc": 'https://fakeimg.pl/150x150',
              "imgAlt": 'Alt vindo de uma variavel',
          },
          {
              "userId": 1,
              "id": 2,
              "title": "quis ut nam facilis et officia qui",
              "completed": false,
              "imgSrc": 'https://fakeimg.pl/150x150',
          },
          {
              "userId": 1,
              "id": 3,
              "title": "fugiat veniam minus",
              "completed": false
          },
          {
              "userId": 1,
              "id": 4,
              "title": "et porro tempora",
              "completed": true
          },
          {
              "userId": 1,
              "id": 5,
              "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
              "completed": false
          }
        ]
      }
    }
}
</script>

<style>
.title {
  font-size: 20px;
  color: blue;
}
.title-home {
  font-size: 40px;
  color: green;
}
.text {
  color: #2c3e50
}
.text-home {
  color: cadetblue;
}
.todos-item {
  background-color: #333;
  margin: 0 0 5px 0;
  padding: 3px 6px;
  color: #fff
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  margin: 60px;
}
</style>
