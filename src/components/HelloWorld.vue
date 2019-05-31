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
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your 哈哈哈哈哈哈哈哈哈哈哈哈哈哈'
    }
  },
  /* eslint-disable */
  mounted () {
    var arr1 = [[0, 1], [2, 6], [4, 5]];
    var element = [3,5,1,2,7,8,4,5,3,4];
    console.log(this.sort(element))
  },
  methods:{
    // 将多维数组变成一维数组的算法
    twechangeone(arr) {
      // console.log(...arr.map(x => Array.isArray(x) ? this.twechangeone(x) : x))
      return [].concat( ...arr.map(x => Array.isArray(x) ? this.twechangeone(x) : x) )
    },
    // 冒泡排序算法的实现代码
    sort(element){
        for(var i = 0;i<element.length-1;i++) {
            for(var j = 0;j<element.length-i-1;j++){
                if(element[j]>element[j+1]){
                    var swap = element[j];
                    element[j] = element[j+1];
                    element[j+1] = swap;
                }
            }
        }
        return element;
    },
    // 取字符串出现次数最多的字符是什么，出现了多少次
    maxString(str){
        var arr = str.split("")
        var obj = {}
        var obj2 = {}
        var max = 1
        for (let i = 0; i < arr.length; i++) {
            var item = arr[i]
            obj[item] = (obj[item]+1) || 1
        }
        for (var key in obj) {
            if (obj[key] > max) {
                max = obj[key]
            }
        }
        for(var key in obj){
            if (obj[key] === max) {
                obj2[key] = max
            }
        }
        return obj2
    }
    /* eslint-eable */
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
