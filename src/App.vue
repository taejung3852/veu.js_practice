<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <div>
    <h4>{{ products[0] }}</h4>
    <p> 50 만원</p>
  </div>
  <div>
    <h4>{{products[1]}}</h4>
    <p>70 만원</p>
  </div>
  <div>
    <h4>{{ products[2] }}</h4>
    <p>90 만원</p>
  </div>
</template>

<script>


export default {
  name: 'App',
  // 데이터 보관소. return 안에 데이터를 입력하면된다. 변수같은거 return 안에 다 넣는다고 생각하면된다. object 자료(키:밸류)로 저장.
  // (중요)이 문법을 언제 왜 쓰는지 배워야한다.
  data(){
    return{
      products : ['신부동원룸', '안서동원룸', '두정동원룸']
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
