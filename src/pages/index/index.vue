<template>
  <div>
    <i-button type="primary" @click="handleClick">这是一个按钮</i-button>
    <i-button @click="handleClick" type="error" long="true">联通两边按钮</i-button>
    <i-button @click="handleClick" type="primary" size="large">Primary</i-button>
    <i-button @click="handleClick" type="ghost" size="default">Ghost</i-button>
    <i-button @click="handleClick" type="info" size="small">Info</i-button>
    <i-button @click="handleClick" type="success" shape="circle"><i-icon type="brush_fill" />Success</i-button>
    <i-button @click="handleClick" type="warning">
      <i-icon type="camera_fill" />
      Warning
    </i-button>
    <i-button @click="handleClick" type="error">Error</i-button>
    
    <i-panel title="基础用法">
      <i-input title="收货人" autofocus placeholder="名字" />
      <i-input type="number" title="联系电话" placeholder="请输入手机号" />
      <i-input type="textarea" title="详细地址" placeholder="请输入详细地址(最多50字)" maxlength="50" />
      <i-input title="用户信息" disabled />
    </i-panel>
    <i-steps>
      <i-step status="finish">
        <view slot="title">
          已完成
        </view>
        <view slot="content">
          这里是该步骤的描述信息
        </view>
      </i-step>
      <i-step status="process">
        <view slot="title">
          进行中
        </view>
        <view slot="content">
          这里是该步骤的描述信息
        </view>
      </i-step>
      <i-step status="">
        <view slot="title">
          错误
        </view>
        <view slot="content">
          这里是该步骤的描述信息
        </view>
      </i-step>
    </i-steps>
    <i-button @click="showModal = true" type="info" size="small">弹出底部action</i-button>
    <i-action-sheet :visible="showModal" :actions="actions" show-cancel @cancel="showModal = false" @click="handleClick" />
  </div>
</template>

<script>
  import card from '@/components/card'

  export default {
    data () {
      return {
        motto: 'Hello miniprograme',
        userInfo: {
          nickName: 'mpvue',
          avatarUrl: 'http://mpvue.com/assets/logo.png'
        },
        showModal: false,
        actions: [{
          name: '选项1'
        }, {
          name: '选项2'
        }, {
          name: '去分享',
          icon: 'share',
          openType: 'share'
        }]
      }
    },

    components: {
      card
    },

    methods: {
      handleClick () {
        console.log('iView Weapp使用成功')
      },
      onShareAppMessage () {
        return {
          title: 'iView Weapp',
          imageUrl: 'https://file.iviewui.com/iview-weapp-logo.png'
        }
      },
      bindViewTap () {
        const url = '../logs/main'
        if (mpvuePlatform === 'wx') {
          mpvue.switchTab({ url })
        } else {
          mpvue.navigateTo({ url })
        }
      }
    },
    created () {}
  }
</script>

<style scoped lang="less">

</style>
