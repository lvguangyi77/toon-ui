<template>
  <div class="page-loadmore">
    <p class="page-loadmore__desc">在列表顶端, 按住 - 下拉 - 释放可以获取更多数据</p>
    <p class="page-loadmore__desc">此例请使用手机查看</p>
    <div class="page-loadmore__wrapper" v-el:wrapper :style="{ height: wrapperHeight + 'px' }">
      <toon-loadmore :top-method="loadTop" @top-status-change="handleTopChange">
        <ul class="page-loadmore__list">
          <li v-for="item in list" class="page-loadmore__listitem">{{ item }}</li>
        </ul>
        <div slot="top" class="toon-loadmore__top">
          <span v-show="topStatus === 'loading'">
            <div>加载中...</div>
          </span>
        </div>
      </toon-loadmore>
    </div>
  </div>
</template>

<style lang="css">
  @component-namespace page {
    @component loadmore {
      @descendent desc {
        text-align: center;
        color: #666;
        padding-bottom: 5px;
        &:last-of-type {
          border-bottom: solid 1px #eee;
        }
      }

      @descendent listitem {
        height: 50px;
        line-height: 50px;
        border-bottom: solid 1px #eee;
        text-align: center;
        &:first-child {
          border-top: solid 1px #eee;
        }
      }

      @descendent wrapper {
        overflow: scroll;
      }

    }
  }

  @component toon-loadmore-top {
    span {
      display: inline-block;
      transition: .2s linear;
      vertical-align: middle;

      @when rotate {
        transform: rotate(180deg);
      }
    }
  }
</style>

<script>
  import toonLoadmore from '../components/Pulldown/index.vue'
  export default {
    components: {
      toonLoadmore,
    },
    data() {
      return {
        list: [],
        // allLoaded: false,
        topStatus: '',
        wrapperHeight: 0
      };
    },

    methods: {
      loadTop() {
        setTimeout(() => {
          let firstValue = this.list[0];
          for (let i = 1; i <= 10; i++) {
            this.list.unshift(firstValue - i);
          }
          this.$refs.loadmore.onTopLoaded();
        }, 1500);
      }
    },

    compiled() {
      for (let i = 1; i <= 10; i++) {
        this.list.push(i);
      }
    },

    ready() {
      this.wrapperHeight = document.documentElement.clientHeight - this.$els.wrapper.getBoundingClientRect().top;
    }
  };
</script>
