<template>
  <div id="root">
    <div class="todo-container">
      <h1>用户反馈数据表</h1>
      <div class="add" style="text-align:right;margin:0 20px 20px 0;">
          <el-button type="primary" @click="add()">添加反馈文本</el-button>
      </div>
      <el-dialog title="反馈文本" :visible.sync="visible" align="center">
        <el-form :model="form">
          <el-form-item label="用户" label-width="80px" required>
            <el-input v-model="form.user" autocomplete="off"></el-input>
          </el-form-item>
          <el-form-item label="内容" label-width="80px" required>
            <el-input v-model="form.content" autocomplete="off"></el-input>
          </el-form-item>
        </el-form>
        <div slot="footer" class="dialog-footer">
    <el-button @click="visible = false">取 消</el-button>
    <el-button type="primary" @click="save()">确 定</el-button>
  </div>
</el-dialog>
      <div class="todo-wrap">
        <el-table :data="tableData" style="width: 100%;background-color:red;" border>
          <el-table-column prop="id"  label="索引"  width="100" align="center"></el-table-column>
          <el-table-column prop="user" label="反馈用户"   align="center"></el-table-column>
          <el-table-column prop="text" label="反馈文本"   align="left" :show-overflow-tooltip="true"></el-table-column>
          <el-table-column prop="time" label="反馈时间"   align="center"></el-table-column>
          <el-table-column label="操作" align="center" width="180">
            <template slot-scope="scope">
              <el-button type="danger"
          @click="handleDelete(scope.$index)">删除</el-button>
      </template>
    </el-table-column>
  </el-table>
      </div>
    </div>
  </div>
</template>

<script>
import { totalmem } from 'os'
import MyFooter from './components/MyFooter.vue'
import MyHeader from './components/MyHeader.vue'
import MyList from './components/MyList.vue'
export default {
  name: 'App',
  components: { MyFooter, MyHeader, MyList },
  // 用于list与header交流
  data() {
    return {
      visible:false,
      todos: JSON.parse(localStorage.getItem('todos')) || [],
      show3: false,
      form: {
        user:"",
        content:""
        },
      tableData:[
        {
          id:1,
          user:"张三",
          text:"真好，系统体验良好，非常期待下一次体验。",
          time:"2020.03.01",
        },
        {
          id:2,
          user:"李四",
          text:"整体会感觉良好，下次接着来。",
          time:"2020.08.12",
        },        
        {
          id:3,
          user:"王五",
          text:"大多数的茶饮都很好喝，希望尝遍所有茶饮。",
          time:"2021.01.01",

        },        {
          id:4,
          user:"小刘",
          text:"今天没有开门，感觉很糟，希望下次正常营业。",
          time:"2022.05.20",

        },        
        {
          id:5,
          user:"gemi",
          text:"期待大家一起来。",
          time:"2022.11.01",
        },
        {
          id:6,
          user:"小天",
          text:"不管别人怎么觉得，我觉得挺好喝的，我还要喝。",
          time:"2022.11.01",

        },
        {
          id:7,
          user:"铠甲勇士",
          text:"一年的最后一天了，好好休息，来年接着努力。",
          time:"2022.12.31",

        },
        {
          id:8,
          user:"20000101",
          text:"新年第一天，我要喝龙井",
          time:"2023.01.01",

        },
        {
          id:9,
          user:"2021",
          text:"明早九点，有人一起去吗？",
          time:"2023.02.01",
        },
        {
          id:10,
          user:"要去的喊我",
          text:"组队一起来，有优惠奥",
          time:"2024.03.21",

        },
        {
          id:11,
          user:"天天来",
          text:"普洱茶很好喝，就是有点贵，天天喝喝不起",
          time:"2024.05.01",

        },
      ]
    }
  },
  computed: {
    tot() {
      return this.todos.length
    }
  },
  watch: {
    todos: {
      deep: true,
      handler(value) {
        localStorage.setItem('todos', JSON.stringify(value))
      }
    }
  },
  methods: {
    add(){
      this.visible = true;
    },
    save(){
      if(this.form.content){
        this.tableData.push(
          {
            id:this.tableData.length+1,
            user:this.form.user,
            text:this.form.content,
            time:"2024.05.24"
          }
        )
        this.visible = false
        this.$message({
          showClose: true,
          message: '添加完成',
          type: 'success'
        })
      }
      else{
          this.$message({
          showClose: true,
          message: '文本不能为空',
          type: 'warning'
        })
      }
      
    },
    handleDelete(index){
      this.tableData.splice(index,1)
      // nextTick()
    },
    showit() {
      // alert("showit")
      var t = document.getElementById('MyyList')
      if (t.style.display === 'block') {
        t.style.display = 'none'
      } else {
        t.style.display = 'block'
      }
    },
    saveit() {
      var t = document.getElementById('asd')
      t.add
      this.$message({
        showClose: true,
        message: '保存成功！',
        type: 'success'
      })
    },
    // 添加一个todo
    AddTodo(x) {
      // unshift头部添加
      this.todos.push(x)
    },
    // 勾选一个todo
    checktodo(id) {
      this.todos.forEach((todo) => {
        if (todo.id === id) todo.done = !todo.done
      })
    },
    // 删除
    shanchu(id) {
      this.todos = this.todos.filter(todo => todo.id !== id)
      this.$message({
        showClose: true,
        message: '删除成功！',
        type: 'success'
      })
    },
    // 全选/全不选
    checkalltodo(done) {
      this.todos.forEach((todo) => {
        todo.done = done
      })
    },
    // 清空全部
    ccall() {
      this.todos = this.todos.filter((todo) => {
        return !todo.done
      })
    }
  }
}
</script>

<style lang="scss">
#root {
  .todo-container {
    width: 80%;
    margin: 20px auto;
    border-radius: 20px;

    h1 {
      text-align: center;
      margin:10px 0;
    }

    // .todo-wrap {
    //   #asd {
    //     margin: auto auto;
    //     margin-left: 17%;
    //   }

    //   .bottom {
    //     background-color:#061830;
    //     margin: 20px auto;
    //     width: 100%;
    //     display: flex;
    //     justify-content: space-around;
    //     // border: 1px solid #000000;
    //     box-shadow: 7px 7px 12px rgba(0, 0, 0, 0.4),
    //       -7px -7px 12px rgba(255, 255, 255, 0.657),
    //       inset 0 0 0x rgba(255, 255, 255, .9),
    //       inset 0 0 0 rgba(0, 0, 0, .4);
    //     padding: 20px;

    //     .control {
    //       width: 50px;
    //       height: 100%;
    //       margin: auto 10px;
    //       text-align: center;
    //       writing-mode: lr-tb;
    //     }

    //     .card {
    //       width: 80%;
    //       background-color:#0084a4;
    //     }
    //   }

    // }
  }
}

/* base */
body {
  // background-color: #E2E1E4;
  background-color:#f3f3f3;
}

.btn {
  display: inline-block;
  padding: 4px 12px;
  margin-bottom: 0;
  font-size: 14px;
  line-height: 20px;
  text-align: center;
  vertical-align: middle;
  cursor: pointer;
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.2), 0 1px 2px rgba(0, 0, 0, 0.05);
  border-radius: 4px;
}

.btn-danger {
  color: #fff;
  background-color: red;
  border: 1px solid #bd362f;
}

.btn-danger:hover {
  color: #fff;
  background-color: #bd362f;
}

.btn:focus {
  outline: none;
}

.todo-container {
  width: 1200px;
  margin: 0 auto;
}

.todo-container .todo-warp {
  padding: 10px;
  border: 1px solid #ddd;
  border-radius: 5px;
}

.niceButton4 {
  background-color: skyblue;
  border: none;
  border-radius: 12px;
  color: white;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 4px 2px;
  cursor: pointer;
  transition-duration: 0.4s;
  -webkit-transition-duration: 0.4s;
}

.niceButton4:hover {
  box-shadow: 0 12px 16px 0 rgba(0, 0, 0, .24),
    0 17px 50px 0 rgba(0, 0, 0, .19);
}
</style>
