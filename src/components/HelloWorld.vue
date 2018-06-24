<template>
  <div class="hello">
    <h1>{{ massage }}</h1>

    <input type="text" v-model="msg">

    <button @click="update()">获取数值</button>
    <br>


    <tab :inputValue="msg"></tab>
  </div>
</template>

<script>

import tab from '../components/tab/tab'

var massage='数据实时变更';

export default {

  methods: {
    update: function(){

      alert("当前输入框中值为\""+this.msg+"\"")
    }
  },

  name: 'HelloWorld',
  components:{
    tab
  },
  data(){
    return {
      massage: massage,
      msg: '请输入'
    }
  },

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  font-weight: normal;
}

</style>
