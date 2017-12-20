<template>
  <div>
    <div>calculator</div>
    <div>output</div>
    <div>{{ calcValue }}</div>
    <calc-button :label="'1'" @click.native="add(1)"></calc-button>
    <calc-button :label="'2'" @click.native="add(2)"></calc-button>
    <calc-button :label="'3'" @click.native="add(3)"></calc-button>
    <calc-button :label="'reset'" @click.native="reset()"></calc-button>
  </div>
</template>

<script>
import CalcButton from "@/components/calc-button/calc-button"
export default {
  name: 'Calculator',
  components: {
    CalcButton
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      calcValue: 0
    }
  },
  methods: {
    add (value) {
      this.calcValue = this.calcValue + value
    },
    reset () {
      this.calcValue = 0 
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
