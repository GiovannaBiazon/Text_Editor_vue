<template>
  <div id="app">
    <Editor v-model="data" :image-provider="imageProvider" :width="width" />
    <pre>{{ data }}</pre>
  </div>
</template>

<script>
import Editor from '@/index.js'
// import Editor from '../dist/vue-editor.min'

export default {
  data() {
    return {
      data:
        '<p><img src="http://localhost/img/module_table_bottom.png"></img></p>',
      imageProvider: {
        name: 'aliyun',
        signature: 'ZtpTqzM2c2cJdaIS+N4BeNp6a5E=',
        policy:
          'eyJleHBpcmF0aW9uIjogIjIwMjAtMDYtMThUMDc6MjY6NDJaIiwgImNvbmRpdGlvbnMiOiBbWyJlcSIsICIkYnVja2V0IiwgInlvdWp1YW4tc3RhZ2luZyJdXX0=',
        domain: 'youjuan-staging.oss-cn-hangzhou.aliyuncs.com',
        OSSAccessKeyId: 'LTAI4G3mTGD1eKGFqCJnNL',
      },
    }
  },
  name: 'app',
  props: {
    width: {
      type: String,
      required: false,
    },
  },
  components: {
    Editor,
  },
}
</script>

<style>
#app {
  font-family: 'Helvetica Neue', Helvetica, 'PingFang SC', 'Hiragino Sans GB',
    'Microsoft YaHei', '\5FAE\8F6F\96C5\9ED1', Arial, sans-serif;
  color: #2c3e50;
  margin-top: 60px;
  margin-left: 300px;
  display: flex;
  /* align-items: center; */
  flex-direction: column;
  /* justify-content: center; */
}
</style>
