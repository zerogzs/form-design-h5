<template>
  <div
    class="wg-item wg-switch"
    :class="[item.label.labelPosition==='top'?'flex-column':'align-middle']"
    :style="item.style"
  >
    <div class="wg-title" :style="{width:$util.changeRem(item.label.labelwidth)}">{{item.label.labelTitle}}</div>
    <label class="label" :id="item.key">
      <input type="checkbox" class="wg-switch-input" v-model="item.value" style="display:none" />
      <span class="wg-switch-core"></span>
    </label>
  </div>
</template>
<script>
export default {
  props: {
    item: {
      type: Object,
      required: true
    }
  }
}
</script>
