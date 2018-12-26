<template>
  <div>
    <div>功能列表</div>
      <div>
        <span>名称</span><input v-model="name" name="name"/>
        <span>字段名</span><input v-model="field" name="field"/>
        <span>函数</span><input v-model="realfunc" name="realfunc"/>
        <button @click="add">增加</button>
      </div>
      <div>
        <span>函数列表</span> 
        <select v-model="func" name="func" v-on:change="selectVal">
          <option value="" disabled selected="selected">请选择</option>
          <option v-for="(item) in funcs" v-bind:key="item" >{{item}}</option>
        </select>
        <p>{{func}}</p>
      </div>
  </div>
</template>
<script>
export default {
  name: "enrich",
  data() {
    return {
      funcs: ["function1(arg1,arg2)","function2(arg1)","function3(arg1)"],
      selected:'',
     // name:'',
     // field:'',
      func:'',
      realfunc:''
    };
  },
  methods: {
		selectVal: function(ele) {
            alert(this.func);
            //this.func = ele.target.value;
        },
    add:function(){

    }
      
  }
};
</script>
