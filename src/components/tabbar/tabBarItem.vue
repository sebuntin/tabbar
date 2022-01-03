<template>
  <div class="tab-bar-item">
    <slot
      v-if="!isActive"
      name='item-icon'
    ></slot>
    <slot
      v-else
      name='item-icon-active'
    ></slot>
    <div :class="{active: isActive}">
      <slot name='item-text'></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TabBarItem',
  data() {
    return {
      isActive: true 
    }
  },
}
</script>

<style>
.tab-bar-item {
  flex: 1;
  text-align: center;
  height: 49px;
  color: dimgray;
}
.tab-bar-item img {
  width: 24px;
  height: 24px;
  margin-top: 3px;
  vertical-align: middle;
}
.active {
  color: black;
}
</style>