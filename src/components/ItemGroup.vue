
<template>
  <div class="item-group-warpper">
    <div :class="classz" :style="style">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    style: String,
    lr: Boolean
  },
  data: function () {
    return {
      classz: "item-responsive-group"
    };
  },
  mounted() {
    if (this.lr) {
      this.classz = "item-responsive-group-only-lr";
    }
  }
};
</script>
