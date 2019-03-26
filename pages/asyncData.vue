<template>
  <div>{{name}}</div>
</template>

<script>
import axios from 'axios'
export default {
  async asyncData({ params }) {
    let { data } = await axios.get(`https://api.myjson.com/bins/hbjfa`)
    return { name: data.name }
  },
  data() {
    return {
      name: 'helloworld'
    }
  }
}
</script>
