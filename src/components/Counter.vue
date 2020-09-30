<template>
<div id="example-1">
  <button @click="upFunction" class="btn btn-info">{{lable}} </button>
  <p v-bind:style="{ fontsize:  fsize = 'px'}">HELLO {{counter}}</p>
</div>
</template>

<script>
export default {
    data: function() {
        return {
            counter: 0,
            fsize: 50,
        }
  },
  props: {
    lable: String,
},
    methods:{
        upFunction: function(){
            this.counter += 1
            this.fsize +=10

            console.log('counter ='+this.counter);
            console.log('fsize ='+this.fsize);
        },
    },


}


</script>

<style>

</style>