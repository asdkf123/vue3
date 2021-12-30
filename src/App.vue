<template>
  <div class="menu">
    <a>Home</a>
    <a>Products</a>
    <a>About</a>
  </div>
  <img alt="Vue logo" src="./assets/logo.png">
  <div>
    {{logo}}
    <h4>{{ products[0] }}</h4>
    <p>{{ price1 }} 만원</p>
  </div >
  <div>
    <h4>{{ products[1] }}</h4>
    <p>{{ price2 }} 만원</p>
  </div >
  <div>
    <h4>{{ products[2] }}</h4>
    <p>{{ price2 }} 만원</p>
  </div >
</template>

<script>

export default {
  name: 'App',
  data(){
    //데이터 보관함
    //{{}} 쓰는 이유는
    //1. 가변적 data의 처리를 위해
    //2. 실시간 자동 렌더링을 위해
    //3. 웹앱 개발을 위해
    //속성 바인딩은 :로 바인딩 함
    return {
      price1: 60,
      price2: 70,
      products: ['역삼동원룸','천호동원룸','마포구원룸'],
    }
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
</style>
