<template>
  <div class="todo-header">
    <input v-model="title" type="text" placeholder="输入茶叶评论(格式 茶叶名:评论内容)" @keyup.enter="add">
    <button class="niceButton4" @click="saveit">保存</button>
  </div>
</template>

<script>
import { nanoid } from 'nanoid'
export default {
  name: 'MyHeader',
  props: ['AddTodo'],
  data() {
    return {
      title: ''
    }
  },
  methods: {
    add() {
      // 校验数据
      if (!this.title.trim()) {
        this.$message({
          showClose: true,
          message: '输入不能为空！',
          type: 'warning'
        })
      }
      else {
        // 将用户输入包装成一个todo对象
        // console.log(e.target.value)
        const todoObj = { id: nanoid(), title: this.title, done: false }
        // console.log(todoObj)
        // 通知app去添加一个todo对象
        this.AddTodo(todoObj)
        // e.target.value=''
        // 清空输入
        this.title = ''
        this.$message({
          showClose: true,
          message: '保存成功！',
          type: 'success'
        })
      }
    },
    saveit() {
      this.add()
    }
  }
}
</script>

<style scoped lang="scss">
/* header */
.todo-header input {
  width: 560px;
  height: 48px;
  font-size: 14px;
  border: 1px solid #ccc;
  padding: 0 20px;
}

.todo-header input:focus {
  outline: none;
  border-color: rgba(82, 168, 236, 0.8);
  box-shadow: inset 0 1px rgba(0, 0, 0, 0.075), 0 0 8px rgba(8, 168, 236, 0.6);
}

.niceButton4 {
  color: white;
  padding: 14px 32px;
  text-align: center;
  display: inline-block;
  font-size: 16px;
  margin: 0 0;
  border-radius: 0;
  cursor: pointer;
  transition-duration: 0.4s;
  -webkit-transition-duration: 0.4s;
}

.niceButton4:hover {
  box-shadow: 0 12px 16px 0 rgba(0, 0, 0, .24),
    0 17px 50px 0 rgba(0, 0, 0, .19);
}
</style>
