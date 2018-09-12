<template>
    <div class="click-counter">
        <div class="counter-num">
            次数：{{num}}
        </div>
        <button class="counter-btn" @click="handleClick">点我呀</button>
        <button class="counter-reset-btn" @click="handleResetClick">重置</button>
    </div>
</template>

<script>
export default {
  props: {
    initNum: {
      type: Number,
      default: 0
    }
  },
  data () {
    return {
      num: this.initNum
    }
  },
  methods: {
    handleClick () {
      this.num += 1
    },
    handleResetClick () {
      this.num = 0
    }
  }
}
</script>

<style>
.click-counter {
  display: flex;
  align-items: center;
  justify-content: center;
  border: 1px solid red;
  background-color: #ffffff;
  padding: 10px;
  width: 80%;
}
.counter-num, .counter-btn, .counter-reset-btn {
  flex: 1;
  margin: 3px;
  font-size: 14px;
}
</style>


