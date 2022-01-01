<template>
  <div class="menu">
    <a v-for="MenuName in NameList" :key="MenuName">{{MenuName}}</a>
  </div>

  <div v-for="(a1,a2) in products" :key="a1">
    <h4>{{ products[a2] }}</h4>
    <p>{{ price[a2] }} 만원</p>
    <button @click="ReportCount[a2]++">허위매물신고</button><span>신고수 : {{ReportCount[a2] }}</span>
  </div >


</template>

<script>


export default {
  name: 'App',
  data(){
    //속성 바인딩은 :로 바인딩 함
    return {
      ReportCount: [0,0,0],
      price: [60,70,80],
      products: ['역삼동원룸','천호동원룸','마포구원룸'],
      NameList: ['home', 'shap', 'about']
    }
  },
  methods: {
    increase(){
      this.ReportCount += 1;
    },
  },
  components: {
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}
.menu a{
  color: white;
  padding: 10px;
}

</style>
