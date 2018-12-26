<template>
<div id="example-5">
  <select v-model="selected">
    <option disabled value="">请选择</option>
    <option>A</option>
    <option>B</option>
    <option>C</option>
  </select>
  <span>Selected: {{ selected }}</span>
</div>
</template>
<script>
export default {
  name: "testselect",
  data() {
    return {
      funcs: ["function1(arg1,arg2)","function2(arg1)","function3(arg1)"],
      selected:'',
      func:'',
      realfunc:''
    };
  },
  methods: {
		selectVal: function(ele) {
            alert(this.func);
            //this.func = ele.target.value;
        }
  }
};
</script>