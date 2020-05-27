<template>
  <div class="hello">
    <h1>Hii</h1>
    <input type="text" v-bind:placeholder="placeholder_value" v-model="input_info">
    <h1>{{message}}</h1>
    <button v-on:click="newText">Change me</button>
  </div>
</template>

<script>
export default {
  name: 'practise',
  data: function(){
    return {
      input_info:'',
      message:'',
      placeholder_value:'Type in \'a\' here.'
    }
  }, 
  methods:{
    newText: function(){
      for(var i = 0; i < 30; i++){ // na koji nacin radim ovo ?

      //1 - timout with bind(this) ?
      // setTimeout(function(){
      //   this.message += this.input_info;
      //   }.bind(this),1000);


    //2 - normal timeout
      // setTimeout(function(){
      //   this.message += this.input_info;
      //   },1000);

    // 3 - basic print
      this.message += this.input_info;
      }
    }
  } 
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang='scss'>

</style>

