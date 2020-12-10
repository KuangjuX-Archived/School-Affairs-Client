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
  height: 45px;
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
  height: 45px;
  /* background: #8C9EFF; */
  /* padding-left: 0;
  padding-right: 46px; */
}

button {
  height: 45px;
  width: 45px;
  cursor: pointer;
  position: absolute;
}
.bar1 input {
  /* border: 1px solid #ffffff; */
  border: 0;
  /* border-radius: 5px; */
  background: #8C9EFF;
  color: black;
  /* padding: 5px 10px; */
  line-height: 32px;
  font-size: 16px;
}
.bar1 button {
  right: 0;
  /* border-radius: 0 5px 5px 0; */
  outline: none;
  background: #8C9EFF;
  /* background: #ffffff; */
}
.bar1 button::before {
  content: url("img/search.svg");
}
::-webkit-input-placeholder {
  color: #ffffff;
  font-size: 13px;
}
.classification-list {
  position: absolute;
  z-index: 1000;
  width: 280px;
  left: 20px;
  overflow-y: scroll;
}
.classification-item {
  color: #000000;
  font-size: 15px;
  font-weight: 500;
}
.classification-item:hover {
  color: #42a5f5;
  opacity: 0.7;
  cursor: pointer;
}
@media screen and (max-width: 768px) {
  .form {
    width: 100%;
    padding: 9px 0;
  }
}
</style>