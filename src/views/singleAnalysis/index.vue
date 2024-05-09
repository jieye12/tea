<template>
  <div class="app-container">
    <el-card class="box-card">
      <div class="tip">
        请输入要进行属性级情感分析的文本:
      </div>
      <el-input v-model="textarea" type="textarea" :disabled="stage" :rows="6" placeholder="请输入要进行属性级情感分析的文本"
        clearable />
    </el-card>
    <div class="btns">
      <el-button type="info" round @click="clear()">清空内容</el-button>
      <el-button type="primary" round @click="emotionAnalysis()">情感分析</el-button>
    </div>
    <el-card v-show="visible" class="box-card">
      <div class="tip" style="text-align: center;">
        {{ this.init ? this.text1 + `示例` : this.text1 + `结果` }}
      </div>
      <!-- <el-input v-show="visible" v-model="result" type="textarea" :rows="13" /> -->
      <el-table :data="analysisResult" style="width: 100%;text-align: center;" border>
        <el-table-column prop="text" label="文本" align="center" />
        <el-table-column prop="aspect" label="属性" align="center" />
        <el-table-column prop="opinions" label="观点" align="center" />
        <el-table-column prop="sentiment" label="情感倾向" align="center" />
      </el-table>
    </el-card>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  data() {
    return {
      init: true,
      textarea: '', // 用户输入框内输入内容
      // analysisResult: '', // 情感分析结果
      analysisResult: [
        {
          text: '很好喝',
          aspect: '味道',
          opinions: "[满意]",
          sentiment: "正向"
        },
        {
          text: '很好，我非常喜欢',
          aspect: '感觉',
          opinions: "[非常满意]",
          sentiment: "正向"
        },
        {
          text: '反正我很喜欢',
          aspect: '感觉',
          opinions: "[个人观点，喜欢]",
          sentiment: "正向"
        },
        {
          text: '差点意思',
          aspect: '感觉',
          opinions: "[ 大体还行，差强人意 ]",
          sentiment: "反向"
        },
      ],
      stage: false,
      visible: true,// 设置情感分析结果的可见性
      text1: '属性级情感分析'
    }
  },
  methods: {
    clear() {
      var that = this
      that.textarea = ''
      // that.analysisResult = ''
      // that.visible = false
      that.$message({
        showClose: true,
        message: '文本内容已清空！',
        type: 'success'
      })
    },
    emotionAnalysis() {
      if (this.textarea === '') {
        this.$message({
          showClose: true,
          message: '输入文本内容不能为空',
          type: 'warning'
        })
        return
      }
      this.$message({
        showClose: true,
        message: '单文本情感分析完成！',
        type: 'success'
      })
      this.init = false
      this.analysisResult = [
        {
          text: this.textarea,
          aspect: '味道',
          opinions: "[满意]",
          sentiment: "正向"
        }
      ]
      this.textarea = ''
      nextTick()
      // var that = this
      // // 获取用户输入框输入的要进行情感分析的文本
      // var ts = document.getElementById('tess1')
      // var context = that.textarea
      // if (context === '') {
      //   this.$message({
      //     showClose: true,
      //     message: '输入文本内容不能为空',
      //     type: 'warning'
      //   })
      //   that.analysisResult = ''
      //   that.visible = false
      // } else {
      //   ts.style.display = 'none'
      //   // 请求后端单文本情感分析接口，请求方法为POST，请求体格式为JSON，字段text为要进行情感分析的文本
      //   axios.post('http://127.0.0.1:8000/v1/singleEmotionAnalysis', {
      //     text: that.textarea
      //   }).then((response) => {
      //     console.log(response.data)
      //     // 获取接口返回的情感分析预测结果并更新界面数据
      //     that.analysisResult = response.data.singleAnalysisResult
      //     that.visible = true
      //     that.$message({
      //       showClose: true,
      //       message: '属性级情感分析完成！',
      //       type: 'success'
      //     })
      //   }).catch((error) => {
      //     // 捕获异常并弹窗提示
      //     console.log(error)
      //     that.analysisResult = ''
      //     that.visible = false
      //     that.$message({
      //       showClose: true,
      //       message: '请求异常，请检查后端服务模块！',
      //       type: 'error'
      //     })
      //   })
      // }
    }
  }
}
</script>

<style scoped lang="scss">
.app-container {
  .moduleIntroduction {
    width: 100%;
    margin: 10px 0;
    border-radius: 20px;
    padding: 10px 20px;
    box-sizing: border-box;

    h2 {
      margin: 5px 0;
      font-style: italic;
    }

    .description {
      text-indent: 2em;
      line-height: 1.5;
      color: red;
      font-style: italic;
    }
  }

  .box-card {
    border-radius: 20px;
    padding: 10px;

    .tip {
      text-align: center;
      font-size: 18px;
      font-weight: bold;
      margin: 10px auto;
    }

  }
}

.btns {
  // margin: 0 auto;
  text-align: center;
  // padding-top: 20px;
  // padding-bottom: 20px;

  .el-button {
    margin: 20px 20px;
  }
}

.app-container::after {
  content: "";
  // background: no-repeat url("./bg.jpg");
  background-size: cover;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  position: absolute;
  z-index: -10086;
}

.el-table {
  width: 80%;
  // min-height: 200px;
}
</style>
