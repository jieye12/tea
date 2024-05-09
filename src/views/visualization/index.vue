<template>
  <div class="one">
    <!-- 按钮 -->
    <div class="btns">
      <div class="top button" @click="goToLink('/view/fine_grained')">
        <div class="content">
          <em>数据和情感效果</em>可视化
        </div>
      </div>
      <div class="second">
        <div class="dataing button" @click="goToLink('/view/dataing')">
          <div class="content">
            <em>数据分析</em>可视化
          </div>
        </div>
        <div class="clustering button" @click="goToLink('/view/clustering')">
          <div class="content">
            <em>聚类效果</em>可视化
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      // url: require("../../assets/img/可视化主页面.jpg"),
    };
  },
  mounted() { },
  methods: {
    // 点击之后进行跳转
    goToLink(url) {
      // 使用 $router.push 方法跳转到指定链接
      this.$router.push(url); // 请将 '/your-link' 替换为你想要跳转的实际链接
    },
  },
};
</script>

<style scoped lang="scss">
.one {
  position: relative;
  min-height: calc(100vh - 50px);
  padding: 10px;
  box-sizing: border-box;

  .btns {
    font-size: 28px;
    padding-top: 150px;
    box-sizing: border-box;

    .top {
      margin: auto;
    }

    .second {
      margin: 100px 150px;
      display: flex;
      justify-content: space-between;
    }
  }
}

.one::after {
  content: "";
  background: no-repeat url("../../assets/img/可视化主页面.jpg");
  background-size: cover;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  position: absolute;
  z-index: -10086;
}

.button {
  width: 300px;
  padding: 5px 0;
  box-sizing: border-box;
  text-align: center;
  border: 4px solid transparent;
  border-radius: 16px;
  background-clip: padding-box, border-box;
  background-origin: padding-box, border-box;
  background-image: linear-gradient(to right, #222, #222), linear-gradient(90deg, #8F41E9, #578AEF);

  .content {
    color: #ffffff;
    font-style: italic;

    em {
      color: aqua;
    }
  }
}
</style>
