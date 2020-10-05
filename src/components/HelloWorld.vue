<template>
  <div class="hello">
   fuck
  </div>
</template>

<script>
import AV from '@/lib/serverless'
import Vue from 'vue'
import axios from 'axios'
import VueAxios from 'vue-axios'

Vue.use(VueAxios, axios);
const TestObject = AV.Object.extend('TestObject');

console.log(typeof (TestObject))

let newName = new TestObject;
console.log(newName)
console.log('fuck')
newName.set('words', 'Hello world!');
console.log('fuck')
newName.save().then((newnName) => {
  console.log('保存成功。')
})

axios.get()

export default {
data(){
  return AV
},
  name: 'HelloWorld',
  props: {
    msg: String
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
