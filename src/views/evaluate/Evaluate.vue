<template>
  <div class="all">
    <div class="main-tea">
      <el-card class="left">
        <h2>好评</h2>
        <div class="tea_item_xili">
          <p class="letter_fb">
            <el-button id="xl1" class="next" @click="change1()">茶汤清亮平和</el-button>
            <el-button id="xl2" class="next" @click="change2()">口感温和甘醇</el-button>
            <el-button id="xl3" class="next" @click="change3()">耐泡度不错</el-button>
            <el-button id="xl5" class="next" @click="change4()">品质不错尚好</el-button>
            <el-button id="xl6" class="next" @click="change5()">汤色明亮宜人</el-button>
            <el-button id="xl7" class="next" @click="change6()">茶叶外形好看</el-button>
            <el-button id="xl8" class="next" @click="change7()">香气清新柔和</el-button>
            <el-button id="xl9" class="next" @click="change8()">色香协调性好</el-button>
            <el-button id="xla" class="next" @click="change9()">叶底嫩绿柔软</el-button>
            <el-button id="xlc" class="next" @click="change10()">整体感觉不错</el-button>
            <el-button id="xle" class="next" @click="change11()">原料细嫩成熟</el-button>
            <el-button id="xlf" class="next" @click="change12()">滋味饱满持久</el-button>
          </p>
        </div>
      </el-card>
      <el-card class="right">
        <h2>差评</h2>
        <div class="tea_item_xili">
          <p class="letter_fb">
            <el-button id="xl1" class="next" @click="change13()">茶汤单薄酸涩</el-button>
            <el-button id="xl2" class="next" @click="change14()">口感苦涩一般</el-button>
            <el-button id="xl3" class="next" @click="change15()">耐泡度不够</el-button>
            <el-button id="xl5" class="next" @click="change16()">茶叶品质不佳</el-button>
            <el-button id="xl6" class="next" @click="change17()">汤色浑浊不美观</el-button>
            <el-button id="xl7" class="next" @click="change18()">外形粗糙不美观</el-button>
            <el-button id="xl8" class="next" @click="change19()">香气沉闷持久性差</el-button>
            <el-button id="xl9" class="next" @click="change20()">色香协调性不好</el-button>
            <el-button id="xla" class="next" @click="change21()">叶底粗老有梗</el-button>
            <el-button id="xlc" class="next" @click="change22()">整体青涩一般</el-button>
            <el-button id="xle" class="next" @click="change23()">原料细碎粗老</el-button>
            <el-button id="xlf" class="next" @click="change24()">滋味寡淡苦涩</el-button>
          </p>
        </div>
      </el-card>
    </div>
    <div class="detail">
      <!-- <h2>{{ detail.title1 }}</h2> -->
      <!-- <h2 id="commit">提到原料的评价中有63%觉得原料差，共40条</h2> -->
      <el-card class="boxf2">
        <h3 style="color:red;">{{ detail.title2 }}</h3>
        <div class="table">
          <el-table :data="data" style="width: 100%;text-align: center;" border>
            <el-table-column prop="brand" label="品牌茶叶" align="center" :show-overflow-tooltip="true" width="200px" />
            <el-table-column prop="viewpoint" label="属性观点" align="center" />
            <el-table-column prop="emotional" label="情感倾向" align="center" />
            <el-table-column prop="text" label="文本" align="left" width="400px"
              style="text-overflow: ellipsis;overflow: hidden;white-space: nowrap;" :show-overflow-tooltip="true" />
          </el-table>
        </div>
        <!-- <div>
          <iframe id="iframeBox" src="../../../../../../../../input/观点之茶汤差.html" frameborder="0"
            style="width: 100%; height: 640px" allowfullscreen />
        </div> -->
      </el-card>
    </div>
  </div>
</template>

<script>

export default {
  data() {
    return {
      fileData: '',
      analysisResults: '',
      visible: false,
      detail: {
        title1: "提到原料的评价中有63%觉得原料好，共40条",
        title2: "好评————茶汤好"
      },
      data: [
        {
          brand: "[西竺牌]西岩山罐装乌龙茶",
          viewpoint: "茶汤淡",
          emotional: "负向",
          text: "茶汤淡薄，碎渣多"
        },
        {
          brand: "[陈升福元昌]传世·红票",
          viewpoint: "茶汤淡",
          emotional: "负向",
          text: "老品牌的黑茶，条索粗碎，香沉，茶汤红浓久油亮，通透性不足，滋味甜淡欠浓，稍有杂味，散开醒茶后减弱。"
        },
        {
          brand: "[宝和祥]清风里 生",
          viewpoint: "茶汤淡",
          emotional: "负向",
          text: "第一泡：茶汤淡，略有茶气，无苦涩感，微甜；第二泡：有略微苦涩感，茶汤变浓，柔顺；第三泡：有涩感，柔和，回甜，留有苦涩感。总体评价：比巴达山那一款总体感觉更好，但还是茶气不明显。"
        },
        {
          brand: "[正大]蒙顶甘露",
          viewpoint: "茶汤一般",
          emotional: "负向",
          text: "有一股焦糊的味道，应该是焙火过度所致，茶汤也一般。"
        },
        {
          brand: "[林博士]炭焙铁观音",
          viewpoint: "茶汤单薄",
          emotional: "负向",
          text: "略有蜜香；茶汤单薄，回甘弱。"
        },
        {
          brand: "[金宗北斗]一级水金龟",
          viewpoint: "茶汤亮",
          emotional: "负向",
          text: "还好，给个及格分吧，茶汤不是很亮"
        },
        {
          brand: "[武夷源]商务茶",
          viewpoint: "茶汤浑浊",
          emotional: "负向",
          text: "这款茶品质中下，做工明显有问题，茶汤浑浊，有尖锐刺鼻的酸味,并且一直持续到最后，挥之不去，令人很不舒服。香气也都是酸味。"
        },
        {
          brand: "[拙夫舍]陈年柑普熟茶",
          viewpoint: "茶汤薄",
          emotional: "负向",
          text: "叶质较粗老带梗，微有嫩芽，花香、甜香明显，带有粗老气，茶汤醇和欠厚，两颊微涩，口齿生津，留香较持久，喉韵明显，叶底粗硬。"
        },
        {
          brand: "[雅咪红]有机生晒红茶",
          viewpoint: "茶汤涩",
          emotional: "负向",
          text: "干茶外型稍有欠缺，有滇红特有的甜蜜香，茶汤涩感偏重。"
        },
        {
          brand: "[巅茶]F1完美无缺",
          viewpoint: "茶汤淡",
          emotional: "负向",
          text: "个性温吞，难以让人一见倾心！香气有点焖，茶汤不是非常醇，叶底稍嫌杂乱。所幸茶汤还算饱满，刺激性及茶气尚可，耐泡度及余韵或可弥补其前述之不足！"
        },
        {
          brand: "[斗记茶业]班章大树饼茶",
          viewpoint: "茶汤淡",
          emotional: "负向",
          text: "第一次喝黑茶，根据感觉评一下。干茶很粗糙的样子，8-9级茶的样子，茶梗粗大。茶汤较淡，香气以木香，药香为主，入口无味，茶气不足。叶底活性不足，泡开后更为粗糙，也许黑茶就这样？"
        },
        {
          brand: "[白沙溪]茯缘",
          viewpoint: "茶汤淡",
          emotional: "负向",
          text: "选料普通，内质比较薄弱的茶。香气带清香，留香不持久，容易消失；茶汤薄弱，微苦微涩，有生津。"
        },
        {
          brand: "[百亩顶茶]明前一级 莫干黄芽",
          viewpoint: "茶汤淡",
          emotional: "负向",
          text: "茶汤入口厚重，但有明显的酸涩感，可能跟储存不当有关。"
        },
        {
          brand: "[蜀信]茉莉花毛峰",
          viewpoint: "茶汤淡",
          emotional: "负向",
          text: "干茶较肥壮，挺拔，汤色明亮浅黄，茶汤厚度一般，滋味甜滑，香气较明显。"
        },
        {
          brand: "[茗抱春]特一级霍山黄芽",
          viewpoint: "茶汤酸苦",
          emotional: "负向",
          text: "茶汤橙黄透净，茶汤稍苦还有点酸。。。"
        },
        {
          brand: "[德泓昌]湖北青砖茶",
          viewpoint: "茶汤淡",
          emotional: "负向",
          text: "茶汤红橙明亮，有金圈，有薯香。但是茶汤淡，不耐泡，最多就是两三泡。"
        },
        {
          brand: "[清凝拙斋]水仙",
          viewpoint: "茶汤淡",
          emotional: "负向",
          text: "茶汤橙红，有烟味，粗老气较重，茶汤略苦。"
        },
        {
          brand: "[勐库戎氏]木叶醇·三年陈",
          viewpoint: "茶汤淡",
          emotional: "负向",
          text: "条型可以，茶汤一般"
        },

      ]
    }
  },
  methods: {
    // 细粒度
    change1() {
      this.detail.title2 = "好评————茶汤好"
      var iBox = document.getElementById('iframeBox')
      var commit = document.getElementById('commit')
      iBox.setAttribute('src', '../../../../input/观点之茶汤好.html')
      commit.innerHTML = '提到原料的评价中有62%觉得茶汤好，共36条'
    },
    change2() {
      this.detail.title2 = "好评————口感好"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../input/观点之口感好.html')
    },
    change3() {
      this.detail.title2 = "好评————泡度好"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../input/观点之泡度好.html')
    },
    change4() {
      this.detail.title2 = "好评————品质好"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../input/观点之品质好.html')
    },
    change5() {
      this.detail.title2 = "好评————汤色好"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../input/观点之汤色好.html')
    },
    change6() {
      this.detail.title2 = "好评————外形好"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../input/观点之外形好.html')
    },
    change7() {
      this.detail.title2 = "好评————香气好"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../input/观点之香气好.html')
    },
    change8() {
      this.detail.title2 = "好评————协调好"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../input/观点之协调好.html')
    },
    change9() {
      this.detail.title2 = "好评————叶底好"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../input/观点之叶底好.html')
    },
    change10() {
      this.detail.title2 = "好评————整体好"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../input/观点之整体好.html')
    },
    change11() {
      this.detail.title2 = "好评————原料好"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../input/观点之原料好.html')
    },
    change12() {
      this.detail.title2 = "好评————滋味好"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../input/观点之滋味好.html')
    },

    change13() {
      this.detail.title2 = "差评————滋味差"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../input/观点之滋味差.html')
    },
    change14() {
      this.detail.title2 = "差评————口感差"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../input/观点之口感差.html')
    },
    change15() {
      this.detail.title2 = "差评————泡度差"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../input/观点之泡度差.html')
    },
    change16() {
      this.detail.title2 = "差评————品质差"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../input/观点之品质差.html')
    },
    change17() {
      this.detail.title2 = "差评————汤色差"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../input/观点之汤色差.html')
    },
    change18() {
      this.detail.title2 = "差评————外形差"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../input/观点之外形差.html')
    },
    change19() {
      this.detail.title2 = "差评————香气差"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../input/观点之香气差.html')
    },
    change20() {
      this.detail.title2 = "差评————协调差"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../input/观点之协调差.html')
    },
    change21() {
      this.detail.title2 = "差评————叶底差"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../input/观点之叶底差.html')
    },
    change22() {
      this.detail.title2 = "差评————整体差"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../input/观点之整体差.html')
    },
    change23() {
      this.detail.title2 = "差评————原料差"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../input/观点之原料差.html')
    },
    change24() {
      this.detail.title2 = "差评————滋味差"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../input/观点之滋味差.html')
    }
  }
}
</script>

<style scoped lang="scss">
.next {
  display: inline-block;

  width: 30%;
  margin: 5px;
  text-align: center;
}

.all {
  background-color: rgba(233, 228, 214, 0.24);
}

.main-tea {
  display: flex;
  justify-content: space-around;
  padding: 20px 5px;

  .left,
  .right {
    width: 45%;
    border-radius: 5px;

    h2 {
      text-align: center;
    }
  }

  .left {
    background-color: #ff00002a;

    .next {
      background-color: #ff00002a;
    }

    .next:hover {
      color: #ff0000;
      font-weight: 700;
    }

    .next:visited {
      color: #444;
    }

  }

  .right {
    background-color: #006c870e;

    .next {
      background-color: #006c870e;
      text-align: center;
    }

    .next:hover {
      color: #444400;
      font-weight: 700;
    }
  }
}

.detail {
  padding: 20px 5px;
  margin: 20px;
  border-radius: 20px;
  text-align: center;
  background: url("./b464a43c4b4c5caa24e7f18869d0ccd.jpg");
  background-size: 100%, 100%;

  h2 {
    padding-left: 20px;
    text-align: center;
  }

  h3 {
    color: #000000;
  }
}

.letter_fb {
  color: gray;
  font-size: small;
  position: relative;
  /* left: 50px; */
}

.i1:hover {
  color: darkgoldenrod
}

.boxf2 {
  background-color: rgba(255, 255, 255, 0.3);
  backdrop-filter: blur(10px);
  -webkit-backdrop-filter: blur(3px);
  border-radius: 5px;
  font-family: sans-serif;
  text-align: center;
  line-height: 1;
  /*max-width: 50%;*/
  /*max-height: 50%;*/
  color: #fff;
  /* background-color: burlywood; */
  // height: 600px;
}

a {
  color: #444;
  text-decoration: none;
  font-size: 12px;
  letter-spacing: 3px;
  margin: 5px;
}

/*a:link,a:visited{color:#999;}*/
a:hover {
  color: #569091;
  color: #c19450;
  color: #c0501f;
}

.box {
  /* 重点设置下面两个属性 */
  background-color: rgba(255, 255, 255, 0.3);
  backdrop-filter: blur(10px);
  -webkit-backdrop-filter: blur(5px);
  border-radius: 5px;
  font-family: sans-serif;
  text-align: center;
  line-height: 1;
  /*max-width: 50%;*/
  /*max-height: 50%;*/
  padding: 20px 40px;
  color: #fff;
  z-index: 1;
}
</style>
