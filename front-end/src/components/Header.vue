<template>
  <header id="Header">
    <!-- 添加背景颜色或图片 -->
    <div :style="{ 'background': '#333 url(your-background-image-url.jpg) no-repeat center center', 'background-size': 'cover' }">
      <div class="top-edition">
        <!-- 给图标和文字添加样式 -->
        <span class="icon-text">
          <i class="your-icon-class"></i>
          <span class="edition-label"></span>
        </span>
      </div>
      <div id="word">
        <h1>{{ msg }}</h1>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      msg: "YOLOv8-DEMO",
      activeIndex: "1",
    };
  },
  methods: {},
};
</script>

<style scoped>
#Header {
  position: relative; /* 使内含元素可以相对定位 */
  height: 200px; /* 设置合适的高度以容纳背景图片和内容 */
  overflow: hidden; /* 防止内容溢出 */
  display: flex;
  align-items: center;
  justify-content: center;
  color: #ffffff;
}


#word {
  flex: 1;
  text-align: center;
  margin-top: -35px;
  font-size: 2.8em;
  letter-spacing: 10px;
  line-height: 1.2;
  opacity: 0.8; /* 提供一定的透明度以适应背景 */
}

h1 {
  color: inherit;
  font-weight: bold;
}

/* 新增的顶部左边版块样式 */
.icon-text {
  display: flex;
  align-items: center;
  gap: 10px;
}

.edition-label {
  font-size: 14px;
  color: #333;
  font-weight: 500;
}

/* 若有图标，请替换.your-icon-class为你实际使用的图标类名 */
.your-icon-class {
  font-size: 24px;
  color: #333;
}

/* 如果有菜单栏样式请保留，如果没有可忽略以下代码 */
.el-menu-demo {
  width: 80%;
  margin: 0 auto;
  padding: 0 auto;
}
</style>