<template>
  <tiny-select v-model="value" popper-class="slot-default">
    <tiny-option v-for="item in options" :key="item.value" :label="item.label" :value="item.value">
      <span class="left">{{ item.label }}</span>
      <span class="right">{{ item.value }}</span>
    </tiny-option>
  </tiny-select>
</template>

<script>
import { Select, Option } from '@opentiny/vue'

export default {
  components: {
    TinySelect: Select,
    TinyOption: Option
  },
  data() {
    return {
      options: [
        { value: '选项1', label: '黄金糕' },
        { value: '选项2', label: '双皮奶' },
        { value: '选项3', label: '蚵仔煎' },
        { value: '选项4', label: '龙须面' },
        { value: '选项5', label: '北京烤鸭' }
      ],
      value: ''
    }
  }
}
</script>

<style lang="less" scoped>
.tiny-select {
  width: 280px;
}
.tiny-option {
  .left {
    margin-right: 8px;
  }
  .right {
    color: #8492a6;
    font-size: 12px;
  }
}
</style>
