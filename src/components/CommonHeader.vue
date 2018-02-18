<template>
  <div>
    <h1>CommonHeaderここから↓↓↓</h1>
        <img src="../assets/logo.png">
        <p>{{greet}}</p>
    <h1>CommonHeaderここまで↑↑↑</h1>
  </div>
</template>

<script>
export default {
  data () {
    return {
      greet: 'こんにちは世界！！'
    }
  }
}
</script>
