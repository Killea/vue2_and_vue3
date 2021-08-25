<template>
  <div class="hello">
    <h1>VUE3 {{msg}} {{ a }}</h1>
    <button @click="clickButton">Button</button>
  </div>
</template>

<script >
import { ref, onMounted } from 'vue'
export default {
  props: {
    msg: String
  },
  setup() {
    let a = ref(0)
    const clickButton = () => {
      a.value +=1
    }
    onMounted(()=> {
      console.log('vue3 created')
    })
    onMounted(()=> {
      console.log('vue3 created2')
    })
    return {
      a,
      clickButton,
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
