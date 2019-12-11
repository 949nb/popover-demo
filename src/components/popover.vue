<template>
  <div @click.stop="xxx" class="poperover">
    <div class="poperover-wrapper" v-if="visble" @click.stop>
      <slot name="content"></slot>
    </div>
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "Popover",
  data() {
    return {
      visble: false
    };
  },
  methods: {
    xxx() {
      this.visble = !this.visble;
      let x = () => {
        console.log(1)
        this.visble = false
        document.removeEventListener('click', x)
      }
      document.addEventListener('click', x)
    }
  }
};
</script>

<style>
.poperover {
  position: relative;
  border: 1px solid;
  display: inline-block;
}
.poperover-wrapper {
  position: absolute;
  bottom: 100%;
  left: 0;
  border: 1px solid;
}
</style>

