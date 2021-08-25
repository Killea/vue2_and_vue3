<template>
  <div class="hello">
    <h1>VUE2 {{ msg }} {{ a }}</h1>
    <button @click="clickButton">Button</button>
  </div>
</template>

<script>
export default {
  name: "HelloWorld2",
  props: {
    msg: String,
  },
  data() {
    return {
      a: 0,
      arrayList: [1,2,3],
    };
  },
  created() {
    console.log("vue2 created");
    console.log(JSON.stringify(this.arrayList))
  },
  methods: {
    clickButton() {
      this.a += 1;
    },
  },
};
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
