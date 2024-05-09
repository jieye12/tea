<template>
  <div>
    <li>
      <label>
        <!-- <input type="checkbox" :checked="todo.done" @click="handlecheck(todo.id)"/> -->
        <input type="checkbox" :checked="todo.done" @change="handlecheck(todo.id)">
        <!-- 如下代码也可以，但是不建议因为修改了propos -->
        <!-- <input type="checkbox" v-model="todo.done""/> -->
        <span> &nbsp;{{ todo.title }}</span>
      </label>
      <button class="btn btn-danger" @click="itemshanchu(todo.id)">删除</button>
    </li>
  </div>
</template>

<script>
export default {
  name: 'MyItem',
  // 声明接收todo
  props: ['todo', 'checktodo', 'shanchu'],
  methods: {
    // 取消勾选
    handlecheck(id) {
      // console.log(id)
      // 通知App将对应的done值取反
      this.checktodo(id)
    },
    // 删除
    itemshanchu(id) {
      this.shanchu(id)
    }
  }
}

</script>

<style lang="scss">
/* item */
li {
  padding: 5px 20px;
  list-style: none;
  height: 50px;
  line-height: 50px;
  box-sizing: border-box;
}

li label {
  height: 50px;
  float: left;
  cursor: pointer;
}

li label input {
  vertical-align: middle;
  zoom: 150%;
  margin-right: 6px;
  position: relative;
  top: -1px;
}

li button {
  float: right;
  display: none;
  margin-top: 3px;
}

li:before {
  content: initial;
}

li:last-child {
  border-bottom: none;
}

li:hover {
  background-color: #ddd;
}

li:hover button {
  display: block;
}
</style>
