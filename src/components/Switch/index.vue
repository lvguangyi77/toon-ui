<template>
  <div class="mint-switch" @click="value = !value">
    <input class="mint-switch-input" type="checkbox" v-model="value">
    <span class="mint-switch-core"></span>
    <div class="mint-switch-label"><slot></slot></div>
  </div>
</template>

<script>
/**
 * mt-switch
 * @module components/switch
 * @desc 切换按钮
 * @param {boolean} [value] - 绑定值，支持双向绑定
 * @param {slot} - 显示内容
 *
 * @example
 * <mt-switch :value.sync="value"></mt-switch>
 */
export default {
  name: 'mt-switch',

  props: {
    value: Boolean
  }
};
</script>

<style>
  .mint-switch {

      display: -webkit-box;

      display: -ms-flexbox;

      display: flex;

      -webkit-box-align: center;

          -ms-flex-align: center;

              align-items: center;

      position: relative
  }

  .mint-switch-label {

      margin-left: 10px;

      display: inline-block
  }

  .mint-switch-label:empty {

      margin-left: 0
  }

  .mint-switch-core {

      display: inline-block;

      position: relative;

      width: 52px;

      height: 32px;

      border: 1px solid #d9d9d9;

      border-radius: 16px;

      box-sizing: border-box;

      background: #d9d9d9
  }

  .mint-switch-core::after, .mint-switch-core::before {

      content: " ";

      top: 0;

      left: 0;

      position: absolute;

      -webkit-transition: -webkit-transform .3s;

      transition: -webkit-transform .3s;

      transition: transform .3s;

      transition: transform .3s, -webkit-transform .3s;

      border-radius: 15px
  }

  .mint-switch-core::after {

      width: 30px;

      height: 30px;

      background-color: #fff;

      box-shadow: 0 1px 3px rgba(0, 0, 0, .4)
  }

  .mint-switch-core::before {

      width: 50px;

      height: 30px;

      background-color: #fdfdfd
  }

  .mint-switch-input {

      display: none
  }

  .mint-switch-input:checked + .mint-switch-core {

      border-color: #26a2ff;

      background-color: #26a2ff
  }

  .mint-switch-input:checked + .mint-switch-core::before {

      -webkit-transform: scale(0);

              transform: scale(0)
  }

  .mint-switch-input:checked + .mint-switch-core::after {

      -webkit-transform: translateX(20px);

              transform: translateX(20px)
  }
</style>