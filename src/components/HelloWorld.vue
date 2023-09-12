<template>
  <div class="hello">
    <h1>{{msg}}</h1>
    <span v-text="msg"></span>
  </div>
  <div>{{human.name}}</div>
  <div>{{human.age}}</div>
  <div>{{human.addr}}</div>
  <div>{{arr}}</div>
  <div>{{arr[0]}}</div>
  <div v-if="arr[1] == 10">10입니다.</div>
  <div v-else-if="arr[0] == 12">12입니다.</div>
  <div v-else>10이 아닙니다.</div>
</template>

<script>
export default {
  name: 'HelloWorld',
  /*props: {// 부모의 값을 자식이 찍을 때
    msg: String
  }*/
  data(){
    return{
      msg:"자식에서 값을 보냅니다.",
      human : {
        name: "홍길동",
        age: 150,
        addr: "한양"
      },
      arr:[10,20,30,40,50,60,70,80,90,100],
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
