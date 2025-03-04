<template>
  <!-- class 속성으로 해당 태그의 이름을 붙여줄 수 있다. -->
  <!-- 이 이름의 역할은 css에서 불러와서 꾸며줄 수 있다. -->
  <div class="menu">
    <a v-for="menu in menus" :key="menu">{{menu}}</a>
  </div>

  <div v-for="(_, i) in products" :key="i"> <!--:key 뒤에는 고유한 값을 넣어줘야하기 때문에 i(index)를 넣어주는 것이 좋다.-->
    <h4>{{ products[i] }}</h4>
    <p>{{prices[i]}} 만원</p>
    <button @click=increase(i)>허위매물신고</button> <span>신고수 : {{ reports[i] }}</span>
  </div>
  
</template>

<script>


export default {
  name: 'App',
  // 데이터 보관소. return 안에 데이터를 입력하면된다. 변수같은거 return 안에 다 넣는다고 생각하면된다. object 자료(키:밸류)로 저장.
  // (중요)이 문법을 언제 왜 쓰는지 배워야한다.
  data(){
    return{
      reports : [0, 0, 0],
      products : ['신부동원룸', '안서동원룸', '두정동원룸'],
      menus : ['Home', 'Shop', 'About'],
      prices : [50, 70, 90]
    }
  },
  methods : {
    increase(i){
      this.reports[i]++;
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
}

.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}
.menu a{
  color: white;
  padding:10px;
}
</style>
