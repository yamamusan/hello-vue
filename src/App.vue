<template>
  <div id="appmain">
    <common-header></common-header>

    <h1>routingによる表示ここから↓↓↓</h1>
    <router-view/>
    <h1>routingによる表示ここまで↑↑↑</h1>

    <!-- https://router.vuejs.org/ja/api/router-link.html -->
    <h1>App.vue(下部)はここから↓↓↓</h1>
      <div><router-link to="/">トップページ</router-link></div>
      <div><router-link to="/todo">ToDo管理ページ</router-link></div>
    <h1>App.vue(下部)はここまで↑↑↑</h1>
  </div>
</template>

<script>
import commonHeader from './components/CommonHeader'

export default {
  name: 'App',
  data () {
    return {
      greet: '今日は世界！！'
    }
  },
  components: {
    commonHeader // タグ指定時はケバブケースで。
  }
}
</script>

<style>
#appmain {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.square_btn{
    margin-top: 10px;
    display: inline-block;
    padding: 0.5em 1em;
    text-decoration: none;
    background: #668ad8;/*ボタン色*/
    color: #FFF;
    border-bottom: solid 4px #627295;
    border-radius: 3px;
}
.square_btn:active {/*ボタンを押したとき*/
    -ms-transform: translateY(4px);
    -webkit-transform: translateY(4px);
    transform: translateY(4px);/*下に動く*/
    border-bottom: none;/*線を消す*/
}
</style>
