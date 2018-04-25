<template>
  <section :class="[pannelClass,cname]">
    <h4>-{{ title }}-</h4>
    <slot/>
  </section>
</template>

<script>
export default {
  data() {
    return {
      pannelClass: "pannel"
    };
  },
  props: {
    cname: {
      type: String,
      default: ""
    },
    title: {
      type: String,
      default: ""
    }
  }
};
</script>

<style lang="scss" scoped>
  @import "../../css/element.scss";
  .pannel {
    @include pannel;
  }
</style>