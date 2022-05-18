<template>
  <div class="red-b">
    <!-- スロットを使うと
    HTMLのタグのように
    開始コンポーネントと閉じコンポーネントをつくり
    その中に情報を差し込める
    (コンポーネントも差し込める) -->
    <HomePageLayout>
      <HomePageContent />
    </HomePageLayout>

    <img alt="Vue logo" src="./assets/logo.png">
    <div class="flex-container">
      <CardSample />
      <CardSample />
      <CardSample />
      <CardSample />
      <CardSample />
      <CardSample />
    </div>

    <!-- step3. componentで指定したコンポーネントを
    設定できる
    -->
    <!-- コンポーネント その中に属性をつけられる(props) -->
    <HelloWorld msg="Vue3 start 123"/>

    <!-- 子コンポーネントから渡ってきたイベント -->
    <HelloWorld @customEvent="parentFunction"></Helloworld>
  </div>
</template>

<script>
// JS Vue.js
// 他のコンポーネントをインポートする方法
// step1. importで読み込む
import HelloWorld from './components/HelloWorld.vue'
import CardSample from '@/components/Card/CardSample'
import HomePageLayout from '@/components/HomePageLayout'
import HomePageContent from '@/components/HomePageContent'

export default {
  name: 'App',
  
  // step2. componentsを書いてその中に
  // インポートしたコンポーネントの名前を書く
  components: {
    HelloWorld,
    CardSample,
    CardSample,
    HomePageContent,
    HomePageLayout,
},
  data(){
    return {
      appTest: 'Appコンポーネントの値です'
    }
  },
  methods: {
    parentFunction(){
      console.log('親の関数が実行されます')
    }
  },
  created(){}
}
</script>

<style scoped>
.red-b{
  border: 1px solid red;
}

.flex-container {
	display: flex;
	justify-content: space-around; /*--justify-contentを指定--*/
	
	/*--以下装飾--*/
	background-color: #ffffff;
	border: solid 5px #fb6158;
}
/* styleはcssをかく */
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
