<template>
  <div>
    <input type="text" v-model="inputname" />
    <!-- <button v-on:click="addName">名前を追加</button> -->
    <button @click="addName">名前を追加</button>
    <ul class="nameList">
      <li v-for="(name, index) in names" :key="index">
        {{ name }}
        <button class="innerbutton" @click="deleteName(index)">
          削除
        </button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputname: "",
      names: [],
    }
  },
  methods: {
    addName:function() {
      this.names.push(this.inputname);
      this.inputname = "";
    },
    deleteName:function(index) {
      this.names.splice(index, 1);
    },
  }
}
</script>

<style scoped>
button {
  appearance: none;
  border: 0;
  border-radius: 5px;
  background: #4676d7;
  color: #fff;
  padding: 8px 16px;
  font-size: 16px;
  cursor: pointer;
}

input {
  border-radius: 5px;
  padding: 8px 16px;
  font-size: 16px;
}

ul, ol {
  padding: 0;
  position: relative;
}

ul li, ol li {
  color: #2d8fdd;
  border-left: solid 6px;
  background: #f1f8ff;
  margin-bottom: 3px;
  line-height: 1.5;
  padding: 0.5em;
  list-style: none;
}

.innerbutton {
  position: absolute;
  right: 1em;
}
</style>