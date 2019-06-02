<template>
        <div class='aaa' >
        
          <input v-model="newItem">
          <p v-text="msg"></p>
           <button>提交</button>
          <ul>
           <li v-for="item in items"  v-bind:key="item">{{item}}</li>
          </ul>
      
        </div>
      </template>
      
      <script>
      
      export default {
         name: 'HelloWorld4',
        data () {
          return {
            newItem:'添加newItem',
            title: '这是data中的信息',
            msg: 'Welcome to Your Vue.js App4' ,
            msg2: 'helloworld4',
            // msgFromFather:'111111',
            isShow: true,
            items: ['第一届课程','第二届课程'],
            liClass: 'this is liclass'
          }
        },
        props:['msgFromFather'],
        
        methods:{
         
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
      