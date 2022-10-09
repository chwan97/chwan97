<template>
  <div>

    <div class='p-left-title'>
      =========项目列表=========<br>
    </div>
    <div class='p-icon-gu'>
      CHWAN
      <div class='p-top-right'>
        <div class='p-circle'></div>
        {{ hours }}:{{ minutes }}
      </div>

    </div>
  </div>
</template>

<style>
body {
  padding: 15px;
  background-color: #252525;
  font-weight: 500;
  font-size: 25px;
}

a, a:active, a:visited, a:hover {
  text-underline: none;
  text-decoration: none;
  /*color: #5309CD;*/
}

.p-icon-gu {
  font-size: 100px;
  color: #2030a0;
  border: 5px solid #ddd;
  position: fixed;
  bottom: 20px;
  transform: translateX(-50%);
  left: 50%;
}

.p-circle {
  width: 40px;
  height: 40px;
  border-radius: 100px;
  background-color: #d30000;
  margin-right: 10px;
}

.p-top-right {
  position: absolute;
  right: 20px;
  top: 20px;
  font-size: 40px;
  display: flex;
  color: #d30000;
  align-items: center;
  font-weight: 600;
}

.p-left-title {
  font-size: 25px;
  color: #aaa;
  position: fixed;
  bottom: 150px;
  transform: translateX(-50%);
  left: 50%;
}
</style>

<script lang='js'>
import pad from 'pad'

export default {
  name: 'IndexPage',
  layout: 'blog',
  data() {
    return {
      hours: '--',
      minutes: '--',
    }
  },
  computed: {},
  methods: {},
  mounted() {
    setImmediate(() => {
      this.hours = pad(2, (new Date()).getHours(), '0')
      this.minutes = pad(2, (new Date()).getMinutes(), '0')
    }, 1000)
  },
}
</script>
