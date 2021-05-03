<template>
  <component :is="tag" :class="size">
    <slot />
  </component>
</template>

<script>
export default {
  name: "CustomText",
  props: {
    tag: {
      type: String,
      default: "span",
    },
    size: {
      type: String,
      default: "normal",
      validator: function (value) {
        return ["xlarge","large","normal", "small", "xsmall", "xxsmall"].indexOf(value) !== -1;
      },
    },
  },
};
</script>

<style scoped>
.large {
  font-size: 14px;
}
.xlarge {
  font-size: 16px;
}
.xllarge {
  font-size: 18px;
}
.xxlarge {
  font-size: 28px;
}
.small {
  font-size: 12px;
}
.xsmall {
  font-size: 11px;
}
.xxsmall {
  font-size: 10px;
}
</style>
