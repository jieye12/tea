<template>
  <div v-show="totle" class="todo-footer">
    <div class="percentage">
      <span style="color:rgb(18,19,51)">已选中：</span>
      <span class="first">{{ donett }}</span>
      <span class="second">/</span>
      <span class="third">{{ totle }}</span>
      <!-- <span></span> -->
    </div>
    <label>
      <input type="checkbox" :checked="isAll" @change="checkall">
      <span>全选</span>
    </label>
    <button class="btn btn-danger" @click="claerall">清除所有评论</button>
  </div>
</template>

<script scoped>

export default {
  name: 'MyFooter',
  props: ['todos', 'checkalltodo', 'ccall'],
  computed: {
    totle() {
      return this.todos.length
    },
    donett() {
      // 方法1 foreach遍历
      // let i =0;
      // this.todos.forEach((todo) => {
      //     if(todo.done) i++
      // });
      // return i

      // 方法2 reduce  pre是上一个值，current是当前值
      //    const x = this.todos.reduce((pre,current)=>{
      //         console.log('@',pre,current)
      //             return pre + (current.done ? 1:0)
      //     },0)
      //     return x
      // 方法2机制精简
      return this.todos.reduce((pre, current) => pre + (current.done ? 1 : 0), 0)
    },
    isAll() {
      return this.donett === this.totle && this.totle > 0
    }
  },
  methods: {
    checkall(e) {
      this.checkalltodo(e.target.checked)
    },
    claerall() {
      this.ccall()
      this.$message({
        showClose: true,
        message: '已全部清除！',
        type: 'success'
      })
    }
  }

}
</script>

<style scoped lang="scss">
/* footer */
.todo-footer {
  line-height: 40px;
  padding: 10px 20px;
  box-sizing: border-box;
  display: flex;
  justify-content: space-between;

  .percentage {

    .first {
      zoom: 150%;
      display: inline-block;
      color: blue;
    }

    .second {
      display: inline-block;
      zoom: 200%;
      color: red;
    }

    .third {
      zoom: 200%;
      color: red;
      zoom: 200%;
      display: inline-block;
    }
  }

  label {
    display: inline-block;
    margin-right: 20px;
    cursor: pointer;

    input {
      position: relative;
      top: -1px;
      zoom: 150%;
      vertical-align: middle;
      margin-right: 5px;
    }
  }

  .todo-footer button {
    float: right;
    margin-top: 5px;
  }
}
</style>
