<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <button @click="information">親に打ち上げる</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    // このコンポーネントが持ってるプロパティ
    // 親から渡せる 受け皿
    msg: String
  },
  data(){
    return { 
      helloworld: 'helloworldのデータです'
    }
  },
  methods: {
    information(){
      // 子から親に打ち上げる
      // 1つめの引数は カスタムイベントの名前
      // 2つめの引数で渡したいデータ
      this.$emit('customEvent', '子からデータを打ち上げました')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
