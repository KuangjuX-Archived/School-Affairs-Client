<template>
    <div class="bar1">
        <div class="form">
            <input
                v-model="content"
                type="text"
                placeholder="请输入您要搜索的内容..."
                name="content"
            >
            <button @click="search()" />
        </div>
  </div>
</template>


<script>
export default {
    name: "SearchColumn",
    data(){
        return{
            content: "",
        }
    },

    methods:{
        search(){
            console.log(this.content)
        }
    }
}
</script>

<style scoped>

.form {
  position: relative;
  height: 32px;
  padding: 0;
  width: 50wh;
}

input,
button {
  border: none;
  outline: none;
  margin: 0;
  padding: 0;
}
input {
  width: 100%;
  height: 32px;
  /* background: #8C9EFF; */
  /* padding-left: 0;
  padding-right: 46px; */
}

button {
  height: 32px;
  width: 32px;
  cursor: pointer;
  position: absolute;
}
.bar1 input {
  /* border: 1px solid #ffffff; */
  border: 0;
  border-radius: 5px;
  /* background: linear-gradient(#B388FF,#5C6BC0); */
  background: #3D5AFE;
  opacity: 0.5;
  color: black;
  /* padding: 5px 10px; */
  line-height: 32px;
  font-size: 16px;
}
.bar1 button {
  right: 0;
  border-radius: 0 5px 5px 0;
  outline: none;
  /* background: linear-gradient(#B388FF,#5C6BC0); */
  /* background: #ffffff; */
  background: #3D5AFE;
  opacity: 0.5;
}
.bar1 button::before {
  content: url("img/search.svg");
}
::-webkit-input-placeholder {
  color: #ffffff;
  font-size: 13px;
}
@media screen and (max-width: 768px) {
  .form {
    width: 100%;
    padding: 9px 0;
  }
}
</style>