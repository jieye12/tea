<template>
  <div class="main-tea">
    <div class="boxf1" v-if="!visible">
      <!--  -->
      <!--  -->
      <el-tabs>
                <el-tab-pane style="min-height: 200px;" label="产地推荐">
          <div class="producer" style="margin: 50px auto;text-align:center;">
            <span>第一梯队：</span>
            <el-button @click="area1()">福建</el-button>
            <el-button @click="area2()">云南</el-button>
            <el-button @click="area3()">四川 </el-button>
            <br>
            <br>
            <span>第二梯队：</span>
            <el-button @click="area4()">台湾</el-button>
            <el-button @click="area5()">湖北</el-button>
            <el-button @click="area6()">浙江</el-button>
            <el-button @click="area7()">安徽</el-button>
            <el-button @click="area8()">广东</el-button>
            <br>
            <br>
            <span>第三梯队：</span>
            <el-button @click="area8()">内蒙古</el-button>
            <el-button @click="area9()">贵州</el-button>
            <el-button @click="area10()">广西</el-button>
            <el-button @click="area11()">江西</el-button>
            <el-button @click="area12()">陕西</el-button>
            <el-button @click="area13()">北京</el-button>
            <br>
            <br>
            <span>第四梯队：</span>
            <el-button @click="area14()">国外</el-button>
            <el-button @click="area15()">河南</el-button>
            <el-button @click="area16()">山东</el-button>
            <el-button @click="area17()">海南</el-button>
            <el-button @click="area18()">山西</el-button>
            <el-button @click="area19()">西藏</el-button>
            <el-button @click="area20()">湖南</el-button>
            <el-button @click="area21()">重庆</el-button>
            <br>
            <br>
            <span>第五梯队：</span>
            <el-button @click="area22()">江苏</el-button>
            <el-button @click="area23()">上海</el-button>
            <el-button @click="area24()">天津</el-button>
            <el-button @click="area25()">宁夏</el-button>
            <el-button @click="area26()">辽宁</el-button>
            <el-button @click="area27()">吉林</el-button>
            <el-button @click="area28()">香港</el-button>
            <el-button @click="area29()">黑龙江</el-button>
            <el-button @click="area30()">甘肃</el-button>
          </div>
        </el-tab-pane>
        <el-tab-pane style="min-height: 200px;" label="属性推荐">
          <div class="letter_fb">
            <div class="all" style="width:700px;margin:0 auto;">              
              <div class="row" style="display:flex;justify-content:space-around;margin:20px auto;">
                  <div id="circle" class="circle">
                    <div class="content" @click=change1()>茶汤好</div>
                  </div>
                  <div id="circle" class="circle">
                  <div class="content" @click=change2()>工艺精细</div>
                  </div>
                  <div id="circle" class="circle">
                    <div class="content" @click=change3()>均匀不错</div>
                  </div>
                  <div id="circle" class="circle">
                    <div class="content" @click=change4()>口感好</div>
                  </div>
                  <div id="circle" class="circle">
                    <div class="content" @click=change5()>耐泡度好</div>
                  </div>
                </div>
              
                            
              <div class="row" style="display:flex;">
                <div class="left" style="">
                    <div id="circle" class="circle" style="margin:45px 0;">
                      <div class="content" @click=change6()>嫩度好</div>
                    </div>
                    <div id="circle" class="circle" style="margin:45px 0;">
                      <div class="content" @click=change7()>色泽好</div>
                    </div>
                </div>
                <div class="center" style="margin:20px;">属性推荐</div>
                <div class="right">
              <div id="circle" class="circle" style="margin:22px 0;">
                <div class="content" @click=change8()>汤色好</div>
              </div>
              <div id="circle" class="circle">
                <div class="content" @click=change9()>甜度好</div>
              </div>
              <div id="circle" class="circle" style="margin:22px 0;">
                <div class="content" @click=change10()>外形好</div>
              </div>
                </div>
                </div>
              <div class="row" style="display:flex;justify-content:space-around;margin:20px auto;">
            <div id="circle" class="circle">
                <div class="content" @click=change11()>香气持久</div>
              </div>
              <div id="circle" class="circle">
                <div class="content" @click=change12()>香气好</div>
              </div>
              <div id="circle" class="circle">
                <div class="content" @click=change13()>选料好</div>
              </div>
              <div id="circle" class="circle">
                <div class="content" @click=change14()>原料好</div>
              </div>
              <div id="circle" class="circle">
                <div class="content" @click=change15()>总体好</div>
              </div>
                </div>
            </div>
            
          </div>
        </el-tab-pane>
        <el-tab-pane style="min-height: 200px;" label="茶类推荐">
          <div class="type">
            <div class="row1">
              <el-button id="q1" @click="cl1()">绿茶 </el-button>
              <el-button id="q2" @click="cl2()">乌龙 </el-button>
              <el-button id="q3" @click="cl3()">红茶 </el-button>
            </div>
            <div class="row2">
              <div class="left">
                <el-button id="q5" @click="cl5()">普洱 </el-button>
                <el-button id="q6" @click="cl6()">黑茶 </el-button>
              </div>
              <div class="center">
                茶类推荐
              </div>
              <div class="right">
                <el-button id="q7" @click="cl7()">速溶 </el-button>
                <el-button id="q8" @click="cl8()">黄茶 </el-button>
              </div>
            </div>
            <div class="row3">
              <el-button id="q9" @click="cl9()">花茶 </el-button>
              <el-button id="q10" @click="cl10()">袋泡</el-button>
              <el-button id="q11" @click="cl11()">普洱</el-button>
            </div>
            <!--  -->
            <!-- <el-button style="color:red">全部 </el-button> -->


          </div>
        </el-tab-pane>

        <el-tab-pane style="min-height: 200px;" label="评分推荐">
          <div class="rate">
              <div @click=pf1()>&gt;9.0</div>
              <div @click=pf2()>8.0~9.0</div>
              <div @click=pf3()>7.0~8.0</div>
              <div @click=pf4()>6.0~7.0</div>
              <div @click=pf5()>&lt;6.0</div>
          </div>
        </el-tab-pane>
      </el-tabs>
      <!--  -->

      <!-- <hr class="line">
      <div class="tea_item_brand">
        <h4 style="color:slateblue;font-size: 20px;font-weight: 700;">茶类推荐</h4>
        <div class="fr">
          <div class="all">
            <div class="letter_fb">
              <span style="color:red">全部 </span>
              <span id="q1" @click="cl1()">绿茶 </span>
              <span id="q2" @click="cl2()">乌龙 </span>
              <span id="q3" @click="cl3()">红茶 </span>
              <span id="q5" @click="cl5()">普洱 </span>
              <span id="q6" @click="cl6()">黑茶 </span>
              <span id="q7" @click="cl7()">速溶 </span>
              <span id="q8" @click="cl8()">黄茶 </span>
              <span id="q9" @click="cl9()">花茶 </span>
              <span id="q10" @click="cl10()">袋泡</span>
            </div>
            <hr class="line">
          </div>
        </div>
      </div>
      <div class="tea_item_chanqu">
        <div>
          <span style="color:cornflowerblue;font-size: 20px;font-weight: 700;">产地推荐</span>
          <span style="font-style: italic;color:grey">(按热门度排序)</span>
        </div>
        <div class="fr">
          <div class="letter_fb">
            <span @click="area1()">福建</span>
            <span @click="area2()">云南</span>
            <span @click="area3()">四川 </span>
            <span @click="area4()">台湾</span>
            <span @click="area5()">湖北</span>
            <span @click="area6()">浙江</span>
            <span @click="area7()">安徽</span>
            <span @click="area8()">广东</span>
            <span @click="area9()">贵州</span>
            <span @click="area10()">广西</span>
            <span @click="area11()">江西</span>
            <span @click="area12()">陕西</span>
            <span @click="area13()">北京</span>
            <span @click="area14()">国外</span>
            <span @click="area15()">河南</span>
            <br><br>
            <span @click="area16()">山东</span>
            <span @click="area17()">海南</span>
            <span @click="area18()">山西</span>
            <span @click="area19()">西藏</span>
            <span @click="area20()">湖南</span>
            <span @click="area21()">重庆</span>
            <span @click="area22()">江苏</span>
            <span @click="area23()">上海</span>
            <span @click="area24()">天津</span>
            <span @click="area25()">宁夏</span>
            <br><br>
            <span @click="area26()">辽宁</span>
            <span @click="area27()">吉林</span>
            <span @click="area28()">香港</span>
            <span @click="area29()">黑龙江</span>
            <span @click="area30()">甘肃</span>
          </div>
          <hr class="line">
        </div>
      </div>
      <div class="tea_item_grade">
        <div style="color:crimson;font-size: 20px;font-weight: 700;">评分推荐</div>
        <div class="fr">
          <p class="letter_fb">
            <span style="color:red;">全部</span>
            <span @click="pf1()">6.0</span>
            <span @click="pf2()">6.0~7.0</span>
            <span @click="pf3()">7.0~8.0</span>
            <span @click="pf4()">8.0~9.0</span>
            <span @click="pf5()">9.0~10.0</span>
          </p>
        </div>
        <hr class="line">
      </div> -->
    </div>
    <div class="box" v-else>
      <el-button @click="ret()"  style="display:block;" plain type="primary">返回</el-button>
      <h1 style="color:#000000;margin:5px 0 20px 0;;">{{ title }}</h1>
      <el-table :data="data" style="width: 100%;text-align: center;" border>
        <el-table-column prop="name" label="茶叶名称" align="center" :show-overflow-tooltip="true" width="200px" />
        <el-table-column prop="brand" label="茶叶品牌" align="center" />
        <el-table-column prop="producer" label="产地" align="center" />
        <el-table-column prop="type" label="类别" align="center" :show-overflow-tooltip="true" />
        <el-table-column prop="rate" label="评分" align="center" :show-overflow-tooltip="true" />
        <el-table-column prop="ranking" label="综合评分排行" align="center" :show-overflow-tooltip="true" />
        <el-table-column prop="link" label="相关链接" align="center" :show-overflow-tooltip="true" />
        <el-table-column prop="viewpoint" label="属性观点" align="center" :show-overflow-tooltip="true" />
        <el-table-column prop="text" label="文本" align="left" :show-overflow-tooltip="true" />
      </el-table>

      <!-- <div>
        <iframe id="iframeBox" src="../../../../细粒度属性推荐/原料好.html" frameborder="0" style="width: 100%; height: 296px"
          allowfullscreen />
      </div> -->
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
      data: [
        {
          name: '特级蒙顶黄芽',
          brand: "美安雅",
          producer: "四川",
          type: "黄茶->蒙顶黄茶",
          rate: '9.2',
          ranking: 24,
          link: "https://chaping.chayu.com/tea/700",
          viewpoint: "原料肥嫩",
          text: "蒙顶山核心产地，高山原生态，传统工艺精制而成。原料肥嫩，色泽黄绿鲜活，，扁平，外形优美，是黄茶中的典范。茶汤甜香、栗香明显，滋味甘醇较滑。"
        },
        {
          name: '杉林溪乌龙',
          brand: "老台湾",
          producer: "台湾",
          type: "乌龙>其他",
          rate: '9.2',
          ranking: 8,
          link: "https://chaping.chayu.com/tea/1474",
          viewpoint: "原料出众",
          text: "这是一款原料出众，工艺优秀，陈化不错的台湾老乌龙。该款产品经过多年的时光陈化，香气已呈现药香，且不失蜜甜香。香气入汤，茶汤甜滑顺爽，且饱满，虽然没有强烈的回甘与生津，但喝完后满口甘凉，齿颊间留淡淡药香。"
        },
        {
          name: '特级蒙顶黄芽',
          brand: "美安雅",
          producer: "四川",
          type: "黄茶->蒙顶黄茶",
          rate: '9.2',
          ranking: 24,
          link: "https://chaping.chayu.com/tea/700",
          viewpoint: "原料肥嫩",
          text: "蒙顶山核心产地，高山原生态，传统工艺精制而成。原料肥嫩，色泽黄绿鲜活，，扁平，外形优美，是黄茶中的典范。茶汤甜香、栗香明显，滋味甘醇较滑。"
        },
        {
          name: '牛肉',
          brand: "孝文家茶",
          producer: "福建",
          type: "乌龙>其他",
          rate: '9.3',
          ranking: 4,
          link: "https://chaping.chayu.com/tea/4276",
          viewpoint: "原料精湛",
          text: "一款山场气息强烈，工艺精湛，香、汤统一协调的顶级山场肉桂。顶级山场原料和精湛中足火工艺让这款牛肉具备了丰厚内质和十足韵味。汤中浅火功香，类似桂皮的植物辛香，甜果香，乳甜香，清花香，综合出一种美妙香氛，伴随着柔和而富有劲道的茶汤，在节奏中变化出糯、滑、甜、爽，还有持久回甘生津和清凉气息，一幅画面浮现，仿若山间的清风，坑谷中的溪涧，山林里的花田，让人沉醉，这画面是静的，也是灵动的，最后一定是满足的，也是回味良久的。"
        },
        {
          name: '红韵圆茶',
          brand: "大益",
          producer: "云南",
          type: "普洱>熟茶",
          rate: '9.1',
          ranking: 231,
          link: "https://chaping.chayu.com/tea/1846",
          viewpoint: "原料细嫩",
          text: "一款选料优质、存放得当的优质熟普。干茶原料细嫩，金毫明显，香气干净通透，枣香浓郁持久，汤水绵稠顺滑，茶汤饱满，回味细腻悠长，茶叶耐泡度好。"
        },
        {
          name: '金斗',
          brand: "斗记茶业",
          producer: "云南",
          type: "普洱>生茶",
          rate: '9.2',
          ranking: 119,
          link: "https://chaping.chayu.com/tea/1051",
          viewpoint: "原料好",
          text: "好的茶，需天时地利人和，即“原料好，工艺好”。金斗，好评度高，大树选料，拼配技术精湛，榜叔自然不能错过，须得喝上一喝，果然汤质饱满，综合协调度高。其风格馥郁甜美，香气高扬盛放，渗入骨骼，草木清香、花香、蜜甜香，依次绽放。而鲜甜筑就滋味的骨架，饱满醇滑的茶汤更添质感。香滋在整个过程中富于变化。进入尾水，亦余香袅袅，甜味依旧，如余音绕梁。"
        },
        {
          name: '金斗极品大树茶',
          brand: "斗记茶业",
          producer: "云南",
          type: "普洱>生茶",
          rate: '9.1',
          ranking: 119,
          link: "https://chaping.chayu.com/tea/380",
          viewpoint: "原料好",
          text: "由西双版纳勐腊地区的极品春茶拼配而成，尤以易武、班章、景迈为主。茶品的原料好，制茶工艺佳，拼配出众，是拼配普洱茶中的杰出之作；茶汤绵稠甜；甜香、花香柔美沉稳，香高馥郁，韵味宽广，耐泡度极好。"
        },
        {
          name: '醇香普洱',
          brand: "佤山映象",
          producer: "云南",
          type: "普洱>熟茶",
          rate: '9.1',
          ranking: 231,
          link: "https://chaping.chayu.com/tea/3241",
          viewpoint: "原料细嫩",
          text: "这款熟茶原料细嫩，香气和滋味表现不俗。香气纯净，枣香、果香、糯香明显，同时伴有干净的米仓香气，香气持续到尾水；滋味则是有持续的甜感，茶汤里香气表现明显，水含香好；茶汤稠滑，饮完口腔带有清凉气息，茶叶耐泡度高。但喉咙稍有发干，回甘生津稍慢。"
        },
        {
          name: '冰岛古树生茶',
          brand: "滇秀",
          producer: "云南",
          type: "普洱>生茶",
          rate: '9.0',
          ranking: 119,
          link: "https://chaping.chayu.com/tea/827",
          viewpoint: "原料选用好",
          text: "干茶：典型的石磨压饼，整个茶饼的颜色比传统定义的冰岛略浅，推断因为含有芽头比较多的缘故。汤色：汤色金黄，明亮度高。气味：香气饱满细腻，带花香，明显存在于喉咙部，能长久保存。滋味：滋味几乎完全无苦，汤水细腻，喝起来有明显冰岛茶的“”，回甜不断。：叶色偏嫩黄，叶质非常油，柔软厚实，可见原料选用好。"
        },
        {
          name: '陈韵金砖',
          brand: "中茶",
          producer: "湖南",
          type: "黑茶>其他",
          rate: '9.0',
          ranking: 129,
          link: "https://chaping.chayu.com/tea/1342",
          viewpoint: "原料浓精细",
          text: "一款优质的陈年茯砖，内质转化的相当不错。原料精细，干茶茂盛。冲泡后茶汤散发着浓郁的陈香，后期还有木质香，整体香气舒适持久。汤质稠厚，带甜，喝完后回甘舒适，喉咙有香，整体口感稳定且耐泡度高。"
        },
        {
          name: '特制雅安藏茶 藏缘',
          brand: "德仁牌",
          producer: "四川",
          type: "黑茶>藏茶",
          rate: '9.0',
          ranking: 431,
          link: "https://chaping.chayu.com/tea/650",
          viewpoint: "原料细嫩",
          text: "干茶：迷你小茶饼形，干茶色泽棕乌，油光泽，圆柱形的菱角，表面平整光洁，茶叶原料细嫩短小，周边略有碎茶末掉落。汤色：汤色橙红明亮，持久度略欠佳。气味：松烟香、焦糖香，后味甜香明显，香味正，高扬，较持久。滋味：茶汤滋味前几泡茶味浓强，后趋于柔和，总体上属于滑、陈醇，厚实感明显。：棕红色且油亮光，较柔软，有点弹性，原料级别尚嫩，但根茎手感稍硬。"
        },
        {
          name: '野生红茶',
          brand: "五指雨林",
          producer: "海南",
          type: "红茶>其他",
          rate: '8.9',
          ranking: 2590,
          link: "https://chaping.chayu.com/tea/1558",
          viewpoint: "原料细嫩",
          text: "是一款原料十分细嫩考究的红茶，花果香特质明显，汤色始终红艳透亮，滋味鲜浓，但是由于原料太过细嫩，整体的耐泡度有所下降，最好的口感只在前三泡得以展现。"
        },
        {
          name: '特级蒙顶黄芽',
          brand: "美安雅",
          producer: "四川",
          type: "黄茶->蒙顶黄茶",
          rate: '9.2',
          ranking: 24,
          link: "https://chaping.chayu.com/tea/700",
          viewpoint: "原料肥嫩",
          text: "蒙顶山核心产地，高山原生态，传统工艺精制而成。原料肥嫩，色泽黄绿鲜活，，扁平，外形优美，是黄茶中的典范。茶汤甜香、栗香明显，滋味甘醇较滑。"
        },
        {
          name: '特级蒙顶黄芽',
          brand: "美安雅",
          producer: "四川",
          type: "黄茶->蒙顶黄茶",
          rate: '9.2',
          ranking: 24,
          link: "https://chaping.chayu.com/tea/700",
          viewpoint: "原料肥嫩",
          text: "蒙顶山核心产地，高山原生态，传统工艺精制而成。原料肥嫩，色泽黄绿鲜活，，扁平，外形优美，是黄茶中的典范。茶汤甜香、栗香明显，滋味甘醇较滑。"
        },
        {
          name: '特级蒙顶黄芽',
          brand: "美安雅",
          producer: "四川",
          type: "黄茶->蒙顶黄茶",
          rate: '9.2',
          ranking: 24,
          link: "https://chaping.chayu.com/tea/700",
          viewpoint: "原料肥嫩",
          text: "蒙顶山核心产地，高山原生态，传统工艺精制而成。原料肥嫩，色泽黄绿鲜活，，扁平，外形优美，是黄茶中的典范。茶汤甜香、栗香明显，滋味甘醇较滑。"
        },
        {
          name: '特级蒙顶黄芽',
          brand: "美安雅",
          producer: "四川",
          type: "黄茶->蒙顶黄茶",
          rate: '9.2',
          ranking: 24,
          link: "https://chaping.chayu.com/tea/700",
          viewpoint: "原料肥嫩",
          text: "蒙顶山核心产地，高山原生态，传统工艺精制而成。原料肥嫩，色泽黄绿鲜活，，扁平，外形优美，是黄茶中的典范。茶汤甜香、栗香明显，滋味甘醇较滑。"
        },
        {
          name: '特级蒙顶黄芽',
          brand: "美安雅",
          producer: "四川",
          type: "黄茶->蒙顶黄茶",
          rate: '9.2',
          ranking: 24,
          link: "https://chaping.chayu.com/tea/700",
          viewpoint: "原料肥嫩",
          text: "蒙顶山核心产地，高山原生态，传统工艺精制而成。原料肥嫩，色泽黄绿鲜活，，扁平，外形优美，是黄茶中的典范。茶汤甜香、栗香明显，滋味甘醇较滑。"
        },
        {
          name: '特级蒙顶黄芽',
          brand: "美安雅",
          producer: "四川",
          type: "黄茶->蒙顶黄茶",
          rate: '9.2',
          ranking: 24,
          link: "https://chaping.chayu.com/tea/700",
          viewpoint: "原料肥嫩",
          text: "蒙顶山核心产地，高山原生态，传统工艺精制而成。原料肥嫩，色泽黄绿鲜活，，扁平，外形优美，是黄茶中的典范。茶汤甜香、栗香明显，滋味甘醇较滑。"
        },
        {
          name: '特级蒙顶黄芽',
          brand: "美安雅",
          producer: "四川",
          type: "黄茶->蒙顶黄茶",
          rate: '9.2',
          ranking: 24,
          link: "https://chaping.chayu.com/tea/700",
          viewpoint: "原料肥嫩",
          text: "蒙顶山核心产地，高山原生态，传统工艺精制而成。原料肥嫩，色泽黄绿鲜活，，扁平，外形优美，是黄茶中的典范。茶汤甜香、栗香明显，滋味甘醇较滑。"
        },
        {
          name: '特级蒙顶黄芽',
          brand: "美安雅",
          producer: "四川",
          type: "黄茶->蒙顶黄茶",
          rate: '9.2',
          ranking: 24,
          link: "https://chaping.chayu.com/tea/700",
          viewpoint: "原料肥嫩",
          text: "蒙顶山核心产地，高山原生态，传统工艺精制而成。原料肥嫩，色泽黄绿鲜活，，扁平，外形优美，是黄茶中的典范。茶汤甜香、栗香明显，滋味甘醇较滑。"
        },
        {
          name: '特级蒙顶黄芽',
          brand: "美安雅",
          producer: "四川",
          type: "黄茶->蒙顶黄茶",
          rate: '9.2',
          ranking: 24,
          link: "https://chaping.chayu.com/tea/700",
          viewpoint: "原料肥嫩",
          text: "蒙顶山核心产地，高山原生态，传统工艺精制而成。原料肥嫩，色泽黄绿鲜活，，扁平，外形优美，是黄茶中的典范。茶汤甜香、栗香明显，滋味甘醇较滑。"
        },
        {
          name: '特级蒙顶黄芽',
          brand: "美安雅",
          producer: "四川",
          type: "黄茶->蒙顶黄茶",
          rate: '9.2',
          ranking: 24,
          link: "https://chaping.chayu.com/tea/700",
          viewpoint: "原料肥嫩",
          text: "蒙顶山核心产地，高山原生态，传统工艺精制而成。原料肥嫩，色泽黄绿鲜活，，扁平，外形优美，是黄茶中的典范。茶汤甜香、栗香明显，滋味甘醇较滑。"
        },
        {
          name: '特级蒙顶黄芽',
          brand: "美安雅",
          producer: "四川",
          type: "黄茶->蒙顶黄茶",
          rate: '9.2',
          ranking: 24,
          link: "https://chaping.chayu.com/tea/700",
          viewpoint: "原料肥嫩",
          text: "蒙顶山核心产地，高山原生态，传统工艺精制而成。原料肥嫩，色泽黄绿鲜活，，扁平，外形优美，是黄茶中的典范。茶汤甜香、栗香明显，滋味甘醇较滑。"
        },
        {
          name: '特级蒙顶黄芽',
          brand: "美安雅",
          producer: "四川",
          type: "黄茶->蒙顶黄茶",
          rate: '9.2',
          ranking: 24,
          link: "https://chaping.chayu.com/tea/700",
          viewpoint: "原料肥嫩",
          text: "蒙顶山核心产地，高山原生态，传统工艺精制而成。原料肥嫩，色泽黄绿鲜活，，扁平，外形优美，是黄茶中的典范。茶汤甜香、栗香明显，滋味甘醇较滑。"
        },
      ],
      title: "观点之原料好"
    }
  },
  methods: {
    ret(){
      this.visible = false
    },
    // 细粒度
    change1() {
      this.visible = true
      this.title = "属性分析————茶汤好"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../细粒度属性推荐/茶汤好.html')
    },
    change2() {
      this.visible = true
      this.title = "属性分析————工艺精细好"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../细粒度属性推荐/工艺精制.html')
    },
    change3() {
      this.visible = true
      this.title = "属性分析————均匀不错"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../细粒度属性推荐/均匀不错.html')
    },
    change4() {
      this.visible = true
      this.title = "属性分析————口感好"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../细粒度属性推荐/口感好.html')
    },
    change5() {
      this.visible = true
      this.title = "属性分析————耐泡度好"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../细粒度属性推荐/耐泡度好.html')
    },
    change6() {
      this.visible = true
      this.title = "属性分析————嫩度好"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../细粒度属性推荐/嫩度好.html')
    },
    change7() {
      this.visible = true
      this.title = "属性分析————色泽好"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../细粒度属性推荐/色泽好.html')
    },
    change8() {
      this.visible = true
      this.title = "属性分析————汤色好"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../细粒度属性推荐/汤色好.html')
    },
    change9() {
      this.visible = true
      this.title = "属性分析————甜度好"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../细粒度属性推荐/甜度好.html')
    },
    change10() {
      this.visible = true
      this.title = "属性分析————外形好"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../细粒度属性推荐/外形好.html')
    },
    change11() {
      this.visible = true
      this.title = "属性分析————色香持久"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../细粒度属性推荐/色香持久.html')
    },
    change12() {
      this.visible = true
      this.title = "属性分析————香气好"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../细粒度属性推荐/香气好.html')
    },
    change13() {
      this.visible = true
      this.title = "属性分析————选料好"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../细粒度属性推荐/工艺精制.html')
    },
    change14() {
      this.visible = true
      this.title = "属性分析————原料好"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../细粒度属性推荐/原料好.html')
    },
    change15() {
      this.visible = true
      this.title = "属性分析————总体好"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../细粒度属性推荐/总体好.html')
    },
    // 茶类推荐
    cl1() {
      this.visible = true
      this.title = "茶类分析————绿茶"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../茶类推荐/绿茶.html')
    },
    cl2() {
      this.visible = true
      this.title = "茶类分析————乌龙"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../茶类推荐/乌龙.html')
    },
    cl3() {
      this.visible = true
      this.title = "茶类分析————红茶"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../茶类推荐/红茶推荐.html')
    },
    cl5() {
      this.visible = true
      this.title = "茶类分析————普洱"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../茶类推荐/普洱.html')
    },
    cl6() {
      this.visible = true
      this.title = "茶类分析————黑茶"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../茶类推荐/黑茶.html')
    },
    cl7() {
      this.visible = true
      this.title = "茶类分析————速溶"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../茶类推荐/速溶.html')
    },
    cl8() {
      this.visible = true
      this.title = "茶类分析————黄茶"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../茶类推荐/黄茶.html')
    },
    cl9() {
      this.visible = true
      this.title = "茶类分析————花茶"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../茶类推荐/花茶.html')
    },
    cl10() {
      this.visible = true
      this.title = "茶类分析————袋泡"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../茶类推荐/袋泡.html')
    },
    cl11() {
      this.visible = true
      this.title = "茶类分析————普洱"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../茶类推荐/普洱.html')
    },
    // 评分
    pf1() {
      this.visible = true
      this.title = "评分分析————>9分"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../按评分推荐/评分小于6分.html')
    },
    pf2() {
      this.visible = true
      this.title = "评分分析————8~9分"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../按评分推荐/评分6分-7分.html')
    },
    pf3() {
      this.visible = true
      this.title = "评分分析————7~8分"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../按评分推荐/评分7分-8分.html')
    },
    pf4() {
      this.visible = true
      this.title = "评分分析————6~7分"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../按评分推荐/评分8分-9分.html')
    },
    pf5() {
      this.visible = true
      this.title = "评分分析————<6分"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../按评分推荐/评分9分-10分.html')
    },

    // 地区
    area1() {
      this.visible = true
      this.title = "地区分析————福建分析"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../产地推荐/福建茶叶.html')
    },
    area2() {
      this.visible = true
      this.title = "地区分析————云南分析"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../产地推荐/云南茶叶.html')
    },
    area3() {
      this.visible = true
      this.title = "地区分析————四川分析"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../产地推荐/四川.html')
    },
    area4() {
      this.visible = true
      this.title = "地区分析————台湾分析"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../产地推荐/台湾.html')
    },
    area5() {
      this.visible = true
      this.title = "地区分析————湖北分析"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../产地推荐/湖北.html')
    },
    area6() {
      this.visible = true
      this.title = "地区分析————浙江分析"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../产地推荐/浙江.html')
    },
    area7() {
      this.visible = true
      this.title = "地区分析————安徽分析"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../产地推荐/安徽.html')
    },
    area8() {
      this.visible = true
      this.title = "地区分析————广东分析"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../产地推荐/广东.html')
    },
    area9() {
      this.visible = true
      this.title = "地区分析————贵州分析"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../产地推荐/贵州.html')
    },
    area10() {
      this.visible = true
      this.title = "地区分析————广西分析"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../产地推荐/广西.html')
    },
    area11() {
      this.visible = true
      this.title = "地区分析————江西分析"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../产地推荐/江西.html')
    },
    area12() {
      this.visible = true
      this.title = "地区分析————陕西分析"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../产地推荐/陕西.html')
    },
    area13() {
      this.visible = true
      this.title = "地区分析————北京分析"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../产地推荐/北京.html')
    },
    area14() {
      this.visible = true
      this.title = "地区分析————国外分析"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../产地推荐/国外.html')
    },
    area15() {
      this.visible = true
      this.title = "地区分析————河南分析"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../产地推荐/河南.html')
    },
    area16() {
      this.visible = true
      this.title = "地区分析————山东分析"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../产地推荐/山东.html')
    },
    area17() {
      this.visible = true
      this.title = "地区分析————海南分析"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../产地推荐/海南.html')
    },
    area18() {
      this.visible = true
      this.title = "地区分析————福建分析"
      var iBox = document.getElementById('iframeBox')
      alert('没有福建记录，为您提供福建内容')
      iBox.setAttribute('src', '../../../../产地推荐/福建茶叶.html')
    },
    area19() {
      this.visible = true
      this.title = "地区分析————西藏分析"
      var iBox = document.getElementById('iframeBox')
      alert('没有西藏记录，为您提供福建内容')
      iBox.setAttribute('src', '../../../../产地推荐/福建.html')
    },
    area20() {
      this.visible = true
      this.title = "地区分析————湖南分析"
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../产地推荐/湖南.html')
    },
    area21() {
      this.visible = true

      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../产地推荐/重庆.html')
    },
    area22() {
      this.visible = true

      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../产地推荐/江苏.html')
    },
    area23() {
      this.visible = true

      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../产地推荐/上海.html')
    },
    area24() {
      this.visible = true

      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../产地推荐/天津.html')
    },
    area25() {
      this.visible = true

      alert('没有宁夏记录，为您提供福建内容')
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../产地推荐/福建.html')
    },
    area26() {
      this.visible = true

      alert('没有辽宁记录，为您提供福建内容')
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../产地推荐/福建.html')
    },
    area27() {
      this.visible = true

      alert('没有吉林记录，为您提供福建内容')
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../产地推荐/福建.html')
    },
    area28() {
      this.visible = true

      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../产地推荐/香港.html')
    },
    area29() {
      this.visible = true

      alert('没有黑龙江记录，为您提供福建内容')
      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../产地推荐/福建.html')
    },
    area30() {
      this.visible = true

      var iBox = document.getElementById('iframeBox')
      iBox.setAttribute('src', '../../../../产地推荐/甘肃.html')
    }
  }
}
</script>

<style scoped lang="scss">
h1{
  text-align:center;
}

.all{
  margin:0 auto;
  .row{
    margin:0 auto;
  }
  .center{
    width:500px;
    height:200px;
    background-color:#179067;
    text-align:center;
    line-height:200px;
    font-size:50px;
  }
  .circle{
    .content{
      width:100px;
      height:50px;
      text-align:center;
      line-height:50px;
      // background-color:#018d9c;
      background-color:#179067;
      font-weight:700;
      margin:10px;
    }
  }
}
.main-tea {
  position: relative;
  // background-size: 100%, 100%;
  padding: 10px 10px 0 10px;
  min-height: calc(100vh - 50px);
  // background-color:#e2e1e4;
  // background-color:#061830;

  .boxf1 {
    width:90%;
    margin:0 auto;
  
    ::v-deep .el-tabs__nav-scroll {
      width:100%;
      display: flex;
      justify-content:space-around;
      // background-color:;
      // justify-content: center;
    }
    .el-tabs {
      // background: url("./977598c5ac40e3aff9df67b53e51242.jpg");
      margin: 20px auto;
      border-radius: 20px;
      .el-tab-pane{
        // background-color:#061830;
        padding:0;
      }

      // span{
      //   display:inline-block;
      //   width:150px;
      //   height:150px;
      //   // flex:0 0 20%;
      //   // padding:20px;
      //   text-align:center;
      //   line-height:150px;
      //   border-radius:50%;
      //   // color:#ffffff;
      //   border:1px solid #569091;
      //   margin:5px 20px;
      //   // background-color:#569091;
      // }
    }
  }
}
.main-tea::after {
  content: "";
  background: url("./977598c5ac40e3aff9df67b53e51242.jpg") ;
  background-size: cover;
  opacity:0.2;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  position: absolute;
  z-index: -10086;
}
.letter_fb {
  // padding: 10px 20px;

  .el-button {
    width: 100px;
    display: inline-block;
    margin: 2px 5px;
  }
}

.button_1 {
  width: 730px;
  /* margin: 0 auto; */
}

/* .i1:hover{color:darkgoldenrod} */

.el-button {
  color: #444;
  text-decoration: none;
  font-size: 12px;
  letter-spacing: 3px;
  margin: 5px;
}

/*a:link,a:visited{color:#999;}*/
.el-button:hover {
  color: #569091;
  color: #c19450;
  color: #c0501f;
}

.box {
  /* 重点设置下面两个属性 */
  background-color: rgba(255, 255, 255, 0.3);
  background: url("./977598c5ac40e3aff9df67b53e51242.jpg");
  backdrop-filter: blur(10px);
  -webkit-backdrop-filter: blur(5px);
  border-radius: 5px;
  font-family: sans-serif;
  text-align: center;
  line-height: 1;
  padding: 20px 40px;
  color: #fff;
}

.black {
  font-weight: bold;
  margin: 5px;
}
.type{
  width:80%;
  margin:20px auto;
  // font-weight:700;
  .row1,.row3{
    width:60%;
    margin:auto;
    display:flex;
    justify-content:space-around;
    .el-button {
      background-color:#304ffe;
        background-color:#ae94fa;
      background-color:#179067;

        width:100px;
        height:50px;
        font-weight:700;
        font-size:20px;

    }
  }
  .row2{
    display:flex;
    height:200px;
    margin:20px auto;
    .left,.right{
      width:20%;
      text-align:center;
      // background-color:#179067;
      .el-button {
        display:block;
        margin:30px auto;
        background-color:#ae94fa;
      background-color:#179067;

        width:100px;
        height:50px;
        font-weight:700;
        font-size:20px;
      }
    }
    .center{
      flex:1;
      // border:1px solid #061830;
      text-align:center;
      line-height:200px;
      font-size:50px;
      background-color:#179067;

    }
  }
}
.rate{
      width: 400px;
      height: 400px;
      margin:0 auto;
      display: flex;
      flex-direction: column;
      background:
       linear-gradient(to bottom, #cc7497 85%, transparent 95%,transparent 0) center 0%,
       linear-gradient(to bottom, #182843 85%, transparent 95%,transparent 0) center 25%,
       linear-gradient(to bottom, #2e6c8e 85%, transparent 95%,transparent 0) center 50%,
       linear-gradient(to bottom, #0084a4 85%, transparent 95%,transparent 0) center 75%,
       linear-gradient(to bottom, #018d9c 85%, transparent 95%,transparent 0) center 100%;
        background-size: 100% 20%;
        background-repeat: no-repeat;
        clip-path: polygon(50% 0, 100% 100%, 0% 100%);
    }
    .rate >div{
      flex-basis: 25%;
      text-align: center;
      font-size: 20px;
      color: rgba(255,255,255,0.8);
      display: flex;
      justify-content: center;
      align-items: center;
    }
</style>
