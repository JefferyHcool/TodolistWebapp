<template>
<main>
  <div id="app">
    <div class="container">
      <div class="title">
        <h1>Todolist</h1>
      </div>
        <div class="input-add">
          <div class="input">
            <el-input   placeholder="添加待办"></el-input>
          </div>

          <button>
            <i class="el-icon-plus"></i>
          </button>
        </div>
      <div class="fitter">
        <div class="fitters all active ">
          全部
        </div>
        <div class=" fitters done">
          已完成
        </div>
        <div class=" fitters undo">
          未完成
        </div>
      </div>
      <div class="list">
        <div class="item">
          <el-radio v-model="radio"  label="1">洗衣服</el-radio>
        </div>
        <div class="item">
          <el-radio v-model="radio" label="1">买菜</el-radio>
        </div>
         <div class="item">
          <el-radio v-model="radio" label="1">记单词</el-radio>
        </div>
      </div>
   
    </div>
  </div>

</main>

</template>

<script>


export default {
  name: 'App',

  // components: {
  //   HelloWorld
  // }
}
</script>

<style>
*{
    padding:0;
    margin:0;
}

main{
  width: 100%;
  min-height: 100vh;
  background-color: #A8D8EA;
  display: grid;
  align-items: center;
  justify-content: center;
}
.container{
  width: 80%;
  max-width: 1000px;
  background-color: #F9F7F7;
  padding: 48px 28px;
  border-radius: 30px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, .12), 0 0 6px rgba(0, 0, 0, .04)
}
.title{
 text-align: center; 
 padding: 20px 0;
 color: #AA96DA;
}
.input-add {
  display: flex;
  align-items: center;
  margin-bottom: 10px;

}
.input-add input{
  border-radius: 48px;
  border: none;
  outline: none;
   box-shadow: 0 2px 12px 0 rgba(0, 0, 0, 0.1)
}
.input-add button{
  /* position: absolute; */
  /* right: 850px; */
  width: 40px;
  height: 40px;
  border: none;
  border-radius: 50%;
  background-image: linear-gradient( 135deg, #43CBFF 10%, #9708CC 100%);
  cursor: pointer;
  color: white;
}
.fitter{
  display: flex;
  margin: 24px 2px;
 
}
.fitters{
  margin-right: 10px;
  color: #364F6B;
}
.active{
  transform: scale(1.1);
  color: #AA96DA;
}


.item{
  background-color: white;
  margin-bottom: 10px;
  padding: 10px 10px;
  border-radius: 10px;
  transition: transform 0.3s;

}
.item:hover{
  transform: scale(1.05);
}



/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;

} */
  

</style>
