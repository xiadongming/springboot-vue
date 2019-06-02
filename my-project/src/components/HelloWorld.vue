<template>
  <div class='aaa' >
  
    <input v-model="newItem">
    <p v-text="msg"></p>
  
    <ul>
    <li v-for ='item in items' v-bind:key="item.id" v-bind:class="{finlshed: item.isFin}" v-on:click='doThis(item)'>
        <p v-text='item.label'></p>
    </li>
    </ul>
    <button v-on:click="buttonClick">按钮点击事件</button>
    <button v-on:click="clickMe">clickMe点击事件</button><br>
    <button v-on:click="clickMeTwo">clickMe点击事件</button>
  </div>
</template>

<script>

export default {
  // name: 'HelloWorld',
  data () {
    return {
      newItem:'添加newItem',
      title: '这是data中的信息',
      msg: 'Welcome to Your Vue.js App' ,
      msg2: 'helloworld',
      // msgFromFather:'111111',
      isShow: true,
      items: [  
        
      ],
      liClass: 'this is liclass'
    }
  },
  props:['msgFromFather'],
  
  methods:{
    doThis:function(something){
      console.log(something.label)
    },
    buttonClick:function(){
    //  alert("按钮点击事件")
    //  comnewItem
    console.log(this.newItem)
    },
    clickMe: function(){

      alert('clickMe事件'+'==msg2===='+this.msg2)
    },
    clickMeTwo: function(){
      alert(this.msgFromFather)

    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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
