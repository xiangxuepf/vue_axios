<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Essential Links</h2>
    <ul>
      <li>
        <a
          href="https://vuejs.org"
          target="_blank"
        >
          Core Docs
        </a>
      </li>
      <li>
        <a
          href="https://forum.vuejs.org"
          target="_blank"
        >
          Forum
        </a>
      </li>
      <li>
        <a
          href="https://chat.vuejs.org"
          target="_blank"
        >
          Community Chat
        </a>
      </li>
      <li>
        <a
          href="https://twitter.com/vuejs"
          target="_blank"
        >
          Twitter
        </a>
      </li>
      <br>
      <li>
        <a
          href="http://vuejs-templates.github.io/webpack/"
          target="_blank"
        >
          Docs for This Template
        </a>
      </li>
    </ul>
    <h2>Ecosystem</h2>
    <ul>
      <li>
        <a
          href="http://router.vuejs.org/"
          target="_blank"
        >
          vue-router
        </a>
      </li>
      <li>
        <a
          href="http://vuex.vuejs.org/"
          target="_blank"
        >
          vuex
        </a>
      </li>
      <li>
        <a
          href="http://vue-loader.vuejs.org/"
          target="_blank"
        >
          vue-loader
        </a>
      </li>
      <li>
        <a
          href="https://github.com/vuejs/awesome-vue"
          target="_blank"
        >
          awesome-vue
        </a>
      </li>
    </ul>
    <div>9999
    <button type="button" @click="show3">点击</button>
    </div>
  </div>
</template>

<script>
  import axios from 'axios'
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  methods:{
      show1 () {
          console.log('0000')
        this.$axios.get("https://www.hao123.com")
          .then(res=>{
            console.log(res)
          })
          .catch(err=>{
            console.log(err)
          })

      },
    show2 () {
      axios({
        headers: {
          'Content-Type': 'application/x-www-form-urlencoded'
        },
        method: 'post',
        url: '/api/lockServer/search',
        data: Qs.stringify(data)
      })
    },
    show3 () {
          console.log('3333')
      axios({
        headers:{
            "token":"888888"
        },
        method: 'get',
        url:'',
        data:{
            "appkey":"acip"
        }
      }).then(res => {
          console.log(res)
      })
    },
    show4 () {
      console.log('3333')
      axios({
        headers:{
            "Authorization":"Basic YWljcF9hcHA6UVd4aFpHUnBianB2Y0dWdU||"
        },
        method: 'get',
        url:'',
        data:{}
      }).then(res => {
        console.log(res)
      })
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
