<template>
  <div>
    <group title="demo list">
      <div class="demolist">
        <cell url="/demo/toast" title="Toast">
          <span slot="center">简短的消息提示框</span>
          <i class="iconfont" slot="left-icon">&#xe62d;</i>
          <i class="iconfont" slot="right-icon">&#xe93d;</i>
        </cell>
        <cell url="/demo/dialog" title="Dialog">
          <span slot="center">弹出式提示框</span>
          <i class="iconfont" slot="left-icon">&#xe62d;</i>
          <i class="iconfont" slot="right-icon">&#xe93d;</i>
        </cell>
        <cell url="/demo/loading" title="Loading">
          <span slot="center">加载提示框</span>
          <i class="iconfont" slot="left-icon">&#xe62d;</i>
          <i class="iconfont" slot="right-icon">&#xe93d;</i>
        </cell>
        <cell url="/demo/tab" title="tabBar">
          <span slot="center">选项卡</span>
          <i class="iconfont" slot="left-icon">&#xe62d;</i>
          <i class="iconfont" slot="right-icon">&#xe93d;</i>
        </cell>
        <cell url="/demo/pulldown" title="pulldown">
          <span slot="center">下拉刷新</span>
          <i class="iconfont" slot="left-icon">&#xe62d;</i>
          <i class="iconfont" slot="right-icon">&#xe93d;</i>
        </cell>
        <cell url="/demo/lazyload" title="Lazyload">
          <span slot="center">图片懒加载</span>
          <i class="iconfont" slot="left-icon">&#xe62d;</i>
          <i class="iconfont" slot="right-icon">&#xe93d;</i>
        </cell>
        <cell url="/demo/button" title="Button">
          <span slot="center">按钮组件</span>
          <i class="iconfont" slot="left-icon">&#xe62d;</i>
          <i class="iconfont" slot="right-icon">&#xe93d;</i>
        </cell>
        <cell url="/demo/field" title="Field">
          <span slot="center">表单编辑器</span>
          <i class="iconfont" slot="left-icon">&#xe62d;</i>
          <i class="iconfont" slot="right-icon">&#xe93d;</i>
        </cell>
        <cell url="/demo/radio" title="radio">
          <span slot="center">单选框</span>
          <i class="iconfont" slot="left-icon">&#xe62d;</i>
          <i class="iconfont" slot="right-icon">&#xe93d;</i>
        </cell>
        <cell url="/demo/checklist" title="checklist">
          <span slot="center">复选框</span>
          <i class="iconfont" slot="left-icon">&#xe62d;</i>
          <i class="iconfont" slot="right-icon">&#xe93d;</i>
        </cell>
        <cell url="/demo/switch" title="Switch">
          <span slot="center">开关组件</span>
          <i class="iconfont" slot="left-icon">&#xe62d;</i>
          <i class="iconfont" slot="right-icon">&#xe93d;</i>
        </cell>
        <cell url="/demo/tcell" title="Cell">
          <span slot="center">list组件</span>
          <i class="iconfont" slot="left-icon">&#xe62d;</i>
          <i class="iconfont" slot="right-icon">&#xe93d;</i>
        </cell>
        <cell url="/demo/search" title="Search">
          <span slot="center">搜索框组件</span>
          <i class="iconfont" slot="left-icon">&#xe62d;</i>
          <i class="iconfont" slot="right-icon">&#xe93d;</i>
        </cell>
        <cell url="/demo/datetimePicker" title="DatetimePicker">
          <span slot="center">日期选择器</span>
          <i class="iconfont" slot="left-icon">&#xe62d;</i>
          <i class="iconfont" slot="right-icon">&#xe93d;</i>
        </cell>
        <cell url="/demo/pullup" title="pullup">
          <span slot="center">加载更多</span>
          <i class="iconfont" slot="left-icon">&#xe62d;</i>
          <i class="iconfont" slot="right-icon">&#xe93d;</i>
        </cell>
        <cell url="/demo/tabBar" title="tabBar">
          <i class="iconfont" slot="left-icon">&#xe62d;</i>
          <i class="iconfont" slot="right-icon">&#xe93d;</i>
        </cell>
      </div>
    </group>
  </div>
</template>
<script>
import Group from '../components/Group/index.vue'
import Cell from '../components/Cell/index.vue'

export default {
  components: {
    Group,
    Cell
  }
}
</script>
<style>
@import '../styles/demo/demo.css'
</style>

