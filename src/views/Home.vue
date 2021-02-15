<template>
 <div class="d-flex justify-content-center">  
   <h1>{{ans}}</h1>
   <br>
   <br>
   <br>
   <br>
   <br>
  


<button type="button" class="btn btn-primary" data-toggle="modal" data-target="#exampleModal">
  按下會彈出視窗
</button>




<div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title" id="exampleModalLabel">Modal title</h5>
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
      </div>
      <div class="modal-body">
        <h3>{{ans}}</h3>
        <br>
        <br>
        <br>
        <button @click="add">加號</button>
        <button @click="minus">減號</button>
        <button @click="clear">全部清除</button>
      </div>
      
      <div class="modal-footer">
        <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
        <button type="button" class="btn btn-primary">Save changes</button>
      </div>
    </div>
  </div>
</div>

</div>
</template>

<script>
// import $ from 'jquery';
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
 data(){
  
  return{  
        ans:'',
        test:'測試文字',
         }
          
 },
 methods:{
   add(){
     if(this.ans.includes("加號")){
     return
     }else  {this.ans = this.ans.concat("加號")}
   },
   minus(){
     
    this.ans = this.ans.concat("減號")
   },

    clear(){
    this.ans =""
   },

 }

 
 
}
</script>
